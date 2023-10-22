# Video link
 `https://www.youtube.com/watch?v=blYx6VQEPXY&list=PL0tP8lerTbX1PRZvp0DUswYL65nQlw48Y&index=7`

# Installation 
`apt-get install postfix && apt-get install mailutils`

# PostFix Configuration
First take backup main.cf
# ########################  main.cf #############
`nano /etc/postfix/main.cf`

Postfix Config lines

# Add the following lines

`relayhost = [smtp.gmail.com]:587`

`myhostname= your_hostname`

# Location of sasl_passwd we saved
`smtp_sasl_password_maps = hash:/etc/postfix/sasl/sasl_passwd`

# Enables SASL authentication for postfix
`smtp_sasl_auth_enable = yes`

`smtp_tls_security_level = encrypt`

# Disallow methods that allow anonymous authentication
`smtp_sasl_security_options = noanonymous`

# ##############################################
-------------------------------------------------------------------------------------------

# Create a file under /etc/postfix/sasl/

Filename: sasl_passwd

# Add the below line
`[smtp.gmail.com]:587 email@gmail.com:password`

# Give read and write acess only for ROOT user
`chmod 600 sasl_passwd`

# Convert the sasl_password file into db file

`postmap /etc/postfix/sasl/sasl_passwd`   ##it will create `sasl_passwd.db` file

------------------------------------------------------------------------------------------

# To send an email using Linux terminal

`echo "Test Mail" | mail -s "Postfix TEST" otherusergmail@gmail.com`
