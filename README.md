# Mes projets en Pyton

# Le nombre mystère
### Code source : 
max =100

min = 1

import random

nouvellePrtie ="oui"

while nouvellePrtie == "oui" :

    alea = random.randint(min, max)
    
    ####### print("Le nombre aléatoir est : ",alea)
    
    nbEssai =0
    
    repMin = min
    
    repMax = max
    
    while True: 
    
        nbEssai +=1
        
        message = "Deviner le nombre entre "+str(repMin)+" et "+str(repMax)+" \n(les bornes sont incluses): "
        
        reponse = int(input(message))
        
        if reponse < alea and reponse> repMin :
        
            repMin = reponse+1
            
        elif reponse > alea  and reponse < repMax:
        
            repMax = reponse-1
            
        elif reponse > repMax or reponse < repMin :  
        
            nbEssai -=1 
            
            print("Le nombre choisi doit être entre ", repMin," et ",repMax)
            
            print("essai non comptabilisé ")
            
        else:            
        
            message = 'Bravo, Vous avez trouver en '+ str(nbEssai)+' fois'
            
            break
            
    print(message )
    
    nouvellePrtie =input('Deviner un autre nombre? (oui/non)')
    

print('A bientôt')

###########################################
