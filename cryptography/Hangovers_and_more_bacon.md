# URL
https://ringzer0ctf.com/challenges/114
# Concept
* Bacon cipher
* transformation of text (uppercase to A, lower to B)

# Method of Solving 
*we are given a ciphertext in the form of a french paragraph
*we need to convert all uppercase letters to the A to conform to the Bacon cipher, which is made up entirely of A
* We also need to convert the lowercase letters to the letter B
* we can do that with this command
'''''
echo 'VoiCI unE SUpeRbe reCeTtE cONcontee pAR a GrouPe d'ArtistEs culinaiRe, dont le BOn Gout and lE SeNs de LA cLasSe n'esteE n'i is limeEEqUe by LE number DE cAlOries qU'ils PeUVEnt Ingurgiter.
 These virtuosos of the deep fryer show you this little clip full of tasteful taste' | tr '[:upper:]' "A" | tr '[:lower:]' "B" | tr -d " " | tr -d "."| tr -d ","

'''''
* then we can feed the transformed text into a web app that decodes Bacon cipher
'''''
https://www.dcode.fr/bacon-cipher
'''''
