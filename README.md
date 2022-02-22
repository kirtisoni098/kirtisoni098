- 👋 Hi, I’m @kirtisoni098
- 👀 I’m interested in ...cyer security and linux
- 🌱 I’m currently learning ...B.Tech(CSE)
- 💞️ I’m looking to collaborate on ...ethical hacking and linux
- 📫 How to reach me ...jvnkirti@gmail.com

<!---
kirtisoni098/kirtisoni098 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
//FCFS (first come firstsever) code in c++
#include <iostream> 
  using namespace std;
  int main() 
  {
  int i,n,at[50],bt[50],ct[50],tat[50],wt[50]; 
  cout<<"enter the no.of process =";
  cin>>n; 
  cout<<"\narival time take as by deafult:"<<endl;
  for(i=0;i<n;i++) 
  { 
     at[i]=i;
  } 
  for(i=0;i<n;i++)
  {
  at[i]=i;
  cout<<"p["<<i<<"]"<<endl;
  }
  cout<<"\nenter burst time"<<endl;
  for(i=0;i<n;i++)
  {
   cin>>bt[i];
  }
  ct[0]=at[0]+bt[0];
  for(i=1;i<n;i++)
  {
   ct[i]=ct[i-1]+bt[i];
   }
   for(i=0;i<n;i++) 
  { 
  tat[i]=ct[i]-at[i]; 
  }
  wt[0]=0;
  for(i=1;i<n;i++) 
  { 
   wt[i]=tat[i]-bt[i];
  }
   cout<<"process\tat\tbt\tct\ttat\twt"<<endl;
   for(i=0;i<n;i++)
  {
  cout<<"p["<<i<<"]"<<"\t"<<at[i]<<"\t"<<bt[i]<<"\t"<<ct[i]<<"\t"<<tat[i]<<"\t"<<wt[i]<<endl; 
  }
  return 0;
  }
