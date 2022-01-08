//Zagorac Kristina INKI826 - zadacha broj 5 'Transportno pretprijatie'
#include <iostream>
#include <vector>
using namespace std;
int main()
{
    vector<float> kilometri;//niza od decimalni broevi-vekktor
    vector<float> gorivo;
    int kamioni = 0;
    int izbor = 0;
    int b = 0;     //b=broj na kamioni
    float vk = 0;  //vk=vnes na kamioni
    float vg = 0;  //vg=vnes na gorivo
    float d = 0;   //d=vkupen broj na kamioni
    float c = 0;   //c=vkupen broj na gorivo
    
    cout<<"---------------------------------------------------------------------------------------------------"<<endl;
     cout<<"Pretstavena e programa vo koja se prikazhuva odredeni presmetki na edno transportno pretprijatie"<<endl;
    cout<<"---------------------------------------------------------------------------------------------------\n\n"<<endl;
    
    do
    {
            cout<<"1.So odbiranje na broj 1 - Mozhnost za vnesuvanje na nov kamion."<<endl;
            cout<<"2.So odbiranje na broj 2 - Proverka na vkupno pominat pat na site "<<kamioni<<" kamioni i na vkupno potroshenoto gorivo na kamionite."<<endl;
            cout<<"3.So odbiranje na broj 3 - Proverka na prosechno izminatiot pat na kamionite i prosechno potrosheno gorivo po kilometar na kamionite."<<endl;
            cout<<"4.So odbiranje na broj 4 - Proverka na indeks na kamionot so najmnogu pominati kilometri."<<endl;
            cout<<"5.So odbiranje na broj 5 - Proverka na indeks na kamionot so najekonomichna potroshuvachka na gorivo."<<endl;
            cout<<"6.So odbiranje na broj 6 - Mozhnost za iskluchuvanje na programata."<<endl;
            cout<<"Vnesi go vashiot izbor: ";
            cin>>izbor;
            cout<<endl;
        
                if(izbor >= 7 || izbor <= 0)
                {
                    cout<<"\tImate vneseno pogreshen izbor, ve molam obidete se povtorno!\n"<<endl;
                }else{
        // 1
        if(izbor == 1)
        {
            kamioni++;
            
            //Kilometri
                cout<<"Vnesete gi izminatite kilometri na kamionot."<<endl;
                cout<<"Kilometri na kamionot: ";
 		        cin>>vk;
                kilometri.push_back(vk);
                
            //Gorivo
                    cout<<"Vnesete go potroshenoto gorivo na kamionot."<<endl;
                    cout<<"Potrosheno gorivo na kamionot: ";
                    cin>>vg;
                    gorivo.push_back(vg);
        }
        // 2
        else if(izbor == 2)
        {
            if(kamioni < 1)
            {
                cout<<"\nVo listata nemate vneseno broj na kamioni.\n"<<endl;
            }
            else
            {
                for(int i = 0; i < kamioni; i++)
                {
                    d += kilometri[i];
                    c += gorivo[i];
                }
                cout<<"Vkupno izminati se: "<<d<<" kilometri."<<endl;
                cout<<"Vkupno potrosheno e: "<<c<<" litri gorivo"<<endl;
            }
                d = 0;
                c = 0;
        }
        // 3
        else if(izbor == 3)
        {
            if(kamioni < 1)
            {
                cout<<"\nVo listata nemate vneseno broj na kamioni.\n"<<endl;
            }
            else
            {
                for(int i = 0; i < kamioni; i++)
                    {
                        d += kilometri[i];
                        c += gorivo[i];
                    }
                cout<<"Prosechno pominat pat na kamionite iznesuva "<<d/kamioni<<" kilometri."<<endl;
                cout<<"Prosechno potrosheno gorivo na kamionite po kilometar iznesuva: "<<c/kamioni<<" litri."<<endl;
            }
        }
        // 4
        else if(izbor == 4)
        {
            if(kamioni < 1)
            {
                cout<<"\nVo listata nemate vneseno broj na kamioni.\n"<<endl;
            }
            else
            {
                if(kamioni > 1)
                {
                    for(int i = 1; i < kamioni; i++)
                        {
                            if(kilometri[i-1] > kilometri[i])
                                {
                                    b = i;
                                }
                                    else
                                {
                                    b = i+1;
                                }
                        }
                }
                else
                {
                    b = 1;
                }
                    cout<<"Spored podatocite, najmnogu kilometri ima pominato kamionot so broj "<<b<<", i toa: "<<kilometri[b-1]<<" kilometri."<<endl;
            }
        }
        // 5
        else if(izbor == 5)
        {
            if(kamioni < 1)
            {
               cout<<"\nVo listata nemate vneseno broj na kamioni.\n"<<endl;
            }
            else
            {
                if(kamioni > 1)
                {
                    for(int i = 1; i < kamioni; i++)
                        {
                            if(gorivo[i-1] < gorivo[i])
                                {
                                    b = i;
                                }
                                else
                                {
                                    b = i+1;
                                }
                        }
                }
                else
                {
                    b = 1;
                }
            cout<<"Spored podatocite, kamionot so broj "<<b<<" e najekonomichniot kamion so "<<gorivo[b-1]<<" potroshuvachka."<<endl;
            }
        }
            cout<<endl;
    }
    }while(izbor != 6);
        cout<<"---------------------------"<<endl;
        cout<<"\tKraj na programata!"<<endl;
        cout<<"---------------------------"<<endl;
        
        cout<<"VI BLAGODARAM NA VNIMANIETO!"<<endl;
}
