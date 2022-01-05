#include <iostream>
#include <vector>
#include <limits>

using namespace std;
int main(){
    vector<float> kilometri;
    vector<float> gorivo;
    int kamioni = 0;
    float vnesK = 0;
    float vnesG = 0;
    int izbor = 0;
    float vkupenBrKilometri = 0;
    float vkupenBrGorivo = 0;
    bool prodolzi = false;
    int brNaKamion = 0;
    
    do{
        izbor = 0;
        prodolzi = false;
        while(izbor < 1 || izbor > 6){
        cout<<"1. Vnesete nov kamion"<<endl;
        cout<<"2. Proverete vkupno pominat pat na site "<<kamioni<<" kamioni i vkupno potroseno gorivo"<<endl;
        cout<<"3. Proverete go prosecniot izminat pat na kamionite i prosecno potroseno gorivo po kilometar"<<endl;
        cout<<"4. Indeks na kamion so najmnogu pominati kilometri"<<endl;
        cout<<"5. Indeks na kamion so najekonomicna potrosuvacka"<<endl;
        cout<<"6. Iskluci ja programata"<<endl;
        cout<<"Izbor: ";
        cin>>izbor;
        cout<<endl;
        
            if(!cin){
                cin.clear();
                cin.ignore(numeric_limits<::streamsize>::max(),'\n');
                cout<<"\t~~~ Nevaliden vnes ~~~"<<endl;
                cout<<endl;
            }else if(izbor < 1 || izbor > 6){
                cout<<"\t~~~ Vasiot izbor ne e na listata ~~~"<<endl;
                cout<<endl;
                cin.ignore(numeric_limits<::streamsize>::max(),'\n');
                }
        }
        
        // 1
        if(izbor == 1){
            kamioni++;
            
            while(prodolzi == false){
            //Kilometri
            cout<<"Vnesete izminati kilometri na kamionot."<<endl;
            cout<<"Kilometri: ";
            cin>>vnesK;
            if(!cin){
                    cin.clear();
                    cin.ignore(numeric_limits<::streamsize>::max(),'\n');
                    cout<<"\n\t~~~ Nevaliden vnes ~~~"<<endl;
                    cout<<endl;
                }else{
                        prodolzi = true;
                    }
            
            //Gorivo
            if(prodolzi == true){
            prodolzi = false;
            cout<<"Vnesete potroseno gorivo."<<endl;
            cout<<"Gorivo: ";
            cin>>vnesG;
            if(!cin){
                    cin.clear();
                    cin.ignore(numeric_limits<::streamsize>::max(),'\n');
                    cout<<"\n\t~~~ Nevaliden vnes ~~~"<<endl;
                    cout<<endl;
                }else{
                        prodolzi = true;
                        kilometri.push_back(vnesK);
                        gorivo.push_back(vnesG);
                    }
            }
            }
        }
        // 2
        else if(izbor == 2){
            if(kamioni < 1){
                cout<<"Nemate vneseno kamioni vo listata"<<endl;
            }else{
                
                for(int i = 0; i < kamioni; i++){
                    vkupenBrKilometri += kilometri.at(i);
                    vkupenBrGorivo += gorivo.at(i);
                }
                cout<<"Vkupno izminati kilometri: "<<vkupenBrKilometri<<endl;
                cout<<"Vkupno potroseno gorivo: "<<vkupenBrGorivo<<endl;
            }
                vkupenBrKilometri = 0;
                vkupenBrGorivo = 0;
        }
        // 3
        else if(izbor == 3){
            if(kamioni < 1){
                cout<<"Nemate vneseno kamioni vo listata"<<endl;
                
            }else{
            for(int i = 0; i < kamioni; i++){
                    vkupenBrKilometri += kilometri.at(i);
                    vkupenBrGorivo += gorivo.at(i);
                }
            cout<<"Prosecen pominat pat: "<<vkupenBrKilometri/kamioni<<endl;
            cout<<"Prosecna potrosuvacka na gorivo: "<<vkupenBrGorivo/kamioni<<endl;
        }
        }
        // 4
        else if(izbor == 4){
            if(kamioni < 1){
                cout<<"Nemate vneseno kamioni vo listata"<<endl;
            }else{
                if(kamioni > 1){
            for(int i = 1; i < kamioni; i++){
                if(kilometri.at(i-1) > kilometri.at(i)){
                    brNaKamion = i;
                }else{
                    brNaKamion = i+1;
                }
            }
                }else{
                    brNaKamion = 1;
                }
            cout<<"Kamionot broj "<<brNaKamion<<" ima pominato "<<kilometri.at(brNaKamion-1)<<endl;
        }
        }
        // 5
        else if(izbor == 5){
            if(kamioni < 1){
                cout<<"Nemate vneseno kamioni vo listata"<<endl;
            }else{
                if(kamioni > 1){
            for(int i = 1; i < kamioni; i++){
                if(gorivo.at(i-1) < gorivo.at(i)){
                    brNaKamion = i;
                }else{
                    brNaKamion = i+1;
                }
            }
                }else{
                    brNaKamion = 1;
                }
            cout<<"Kamionot broj "<<brNaKamion<<" e najekonomicen so "<<gorivo.at(brNaKamion-1)<<" potrosuvacka"<<endl;
            }
        }
        cout<<endl;
    }while(izbor != 6);
        cout<<"\t~~~ Programata zavrsi ~~~\n\n"<<endl;
}
