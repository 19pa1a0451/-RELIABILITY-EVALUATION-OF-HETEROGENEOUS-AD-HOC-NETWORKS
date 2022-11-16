# -RELIABILITY-EVALUATION-OF-HETEROGENEOUS-AD-HOC-NETWORKS


import java.util.*;
import java.io.*;
import java.lang.*;

public class Main{
    private  final int NO_PARENT = -1;
    String ss="";
    int destination;
    private  void dijkstra(int[][] adjacencyMatrix, int startVertex)
    {
        int nVertices = adjacencyMatrix[0].length;
 
       
        int[] shortestDistances = new int[nVertices];
 
       
        boolean[] added = new boolean[nVertices];
 
       
        for (int vertexIndex = 0; vertexIndex < nVertices;  
                                            vertexIndex++)
        {
            shortestDistances[vertexIndex] = Integer.MAX_VALUE;
            added[vertexIndex] = false;
        }
         
       
        shortestDistances[startVertex] = 0;
 
        // Parent array to store shortest
        // path tree
        int[] parents = new int[nVertices];
 
        // The starting vertex does not  
        // have a parent
        parents[startVertex] = NO_PARENT;
 
        // Find shortest path for all  
        // vertices
        for (int i = 1; i < nVertices; i++)
        {
 
            int nearestVertex = -1;
            int shortestDistance = Integer.MAX_VALUE;
            for (int vertexIndex = 0;
                     vertexIndex < nVertices;  
                     vertexIndex++)
            {
                if (!added[vertexIndex] && shortestDistances[vertexIndex] <  shortestDistance)  
                {
                    nearestVertex = vertexIndex;
                    shortestDistance = shortestDistances[vertexIndex];
                }
            }
 
            if(nearestVertex==-1) {
                nearestVertex=0;
            added[0] = true;
            }else{
                added[nearestVertex] = true;
            }
 
     
            for (int vertexIndex = 0;  vertexIndex < nVertices;  vertexIndex++)  
            {
                int edgeDistance = adjacencyMatrix[nearestVertex][vertexIndex];
                 
                if (edgeDistance > 0&& ((shortestDistance + edgeDistance) <  shortestDistances[vertexIndex]))  
                {
                    parents[vertexIndex] = nearestVertex;
                    shortestDistances[vertexIndex] = shortestDistance +  edgeDistance;
                }
            }
        }
 
        printSolution(startVertex, shortestDistances, parents);
    }
 
    private  void printSolution(int startVertex, int[] distances, int[] parents)
    {
        int nVertices = distances.length;
       
         int vertexIndex = destination;
         
            if (vertexIndex != startVertex)  
            {
                 
                if(distances[vertexIndex] !=Integer.MAX_VALUE){
               
                printPath(vertexIndex, parents);
                }
               
        }
    }
   
    private  void printPath(int currentVertex, int[] parents)
    {
       
        if (currentVertex == NO_PARENT)
        {
            return;
        }
        printPath(parents[currentVertex], parents);
        ss+=currentVertex+" ";
       
    }
       public static void main(String[] args) {
       
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter number of nodes : ");
        int n=sc.nextInt();
        System.out.println("Enter destination node : ");
        int dest=sc.nextInt();
       
        for(int w=10;w<70;w+=10){
             double res=0.0;
            int min = -w;
            int max = w;
           
        for(int p=0;p<8;p++){
        ArrayList<ArrayList<Integer>> cord=new ArrayList<ArrayList<Integer>>();
       
        for(int i=0;i<n;i++){
           
                    int x = (int)Math.floor(Math.random()*(max-min)+min);
                    int y = (int)Math.floor(Math.random()*(max-min)+min);
                    int z=(int)Math.random()*(200-10+1)+10;  
                    ArrayList<Integer> a = new ArrayList<Integer>();
                    a.add(x);
                    a.add(y);
                    a.add(z);
                    cord.add(a);
        }
        int[][] mat=new int[n][n];
       
        for(int i = 0; i <n; i++){
           for(int j=0;j<n;j++){
               if(i!=j){
               int a=cord.get(i).get(0);
               int b=cord.get(i).get(1);
               int c=cord.get(j).get(0);
               int d=cord.get(j).get(1);
               int f=cord.get(i).get(2);
               double dist=Math.sqrt((d - b) * (d - b) + (c - a) * (c - a));
               
               if (dist<=f){
                   int m=(int) dist;
                 
                   mat[i][j]=m;
               }
        }
    }
    }
       Main m=new Main();
       m.destination=dest;
       m.dijkstra(mat, 0);
       
       String str = m.ss;
       String parts[] = str.split(" ");
       
        if(parts.length>1){
        res+=Math.pow(0.9,parts.length);
        }
       
    }
    System.out.println(w+"  "+res/8);
   
}
}
}
