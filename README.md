    bool isIsomorphic(string s, string t) {
        //  char is from 0 to 255 so total char is 256 
        int hash[256] = {0} ; // initialise by 0
        bool istcharMapped[256] = {0}; // for string t, for checking the mapping 
        for( int i =0 ; i<s.size() ; i++){
            if(hash[s[i]] == 0 && istcharMapped[t[i]] ==0){
                hash[s[i]] =t[i] ;
                istcharMapped[t[i]]=true ;
            }
        }
        for( int i =0 ; i<s.size() ; i++){
            if(char(hash[s[i]]) != t[i]){
                return false ;
            }
        }
        return true ;
    }
