//
//  main.cpp
//  chache1
//
//  Created by Josue Aleman on 11/16/17.
//  Copyright © 2017 Josue Aleman. All rights reserved.
//

#include <iostream>
#include <cstring>
#include <bitset>
#include <fstream>

using namespace std;
string hexToBin(char);

int main(){
    bitset<4> my_bits[8];
    
    //testing to convert the bits into int values (working)
    //bitset<4> test_bit (string ("0101"));
    //int test_int=(int)test_bit.to_ulong();
    //cout<<test_int<<endl;
    
    //testing one way of assinging to the bits below (working)
   // string mystring="0110";
    //my_bits[0] =bitset<4>(mystring);
    //cout<<my_bits[0]<<endl;
    
    
    string stringOne, stringTwo, stringThree;
    ifstream inFile;
    inFile.open("test1.txt");
    
    if (!inFile){
        cout << "Unable to open file";
        exit(1); // terminate with error
    };
    while (inFile){
        inFile>>stringOne>>stringTwo>>stringThree;
        cout<<stringOne<<" "<<stringTwo<<" "<<stringThree<<endl;
        
        for( int i=0; i<stringOne.size();i++){
            my_bits[i]=bitset<4> (hexToBin(stringOne[i]));
        }
        
        for( int i=0; i<stringTwo.size();i++){
            my_bits[i+4]=bitset<4> (hexToBin(stringTwo[i]));
        }
        
        for( int i=0; i<stringThree.size();i++){
            my_bits[i+6]=bitset<4> (hexToBin(stringThree[i]));
        }
        for(int i=0;i<8;i++){
            cout<<my_bits[i]<<endl;
            
        }
        
    }
    return 0;
}
string hexToBin(char mychar){
    
    switch (toupper(mychar)) {
        case '0': return "0000";
            break;
        case '1': return "0001";
            break;
        case '2': return "0010";
            break;
        case '3': return "0011";
            break;
        case '4': return "0100";
            break;
        case '5': return "0101";
            break;
        case '6': return "0110";
            break;
        case '7': return "0111";
            break;
        case '8': return "1000";
            break;
        case '9': return "1001";
            break;
        case 'A': return "1010";
            break;
        case 'B': return "1011";
            break;
        case 'C': return "1100";
            break;
        case 'D': return "1101";
            break;
        case 'E': return "1110";
            break;
        case 'F': return "1111";
            break;

        default:return NULL;
            break;
    }
}
