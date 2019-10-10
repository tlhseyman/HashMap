package sample;

import java.util.HashMap;

public class WordCount {
    public static void main(String[] args) {
        String sentence = "There is a great weather outside. Houston's weather is really hot.";
        String[] split = sentence.split(" ");
        HashMap<String, Integer> map = new HashMap<String, Integer>();
        for(int i = 0; i < split.length; i++){
            if(map.containsKey(split[i])){
                map.put(split[i], map.get(split[i])+1);
            }
            else
                map.put(split[i],1);
        }
        System.out.println(map);
    }
}
