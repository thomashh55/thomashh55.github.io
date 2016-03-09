---
title: "Assignment_4"
date: 2015-05-23
---

The goal was to create production system, that would learn rules and derive new rules from them.

<!--excerpt--> 

System loaded rules from a file and by their combinations derived new rules over and over until no new rules could be found.

*[Here is the documentation]({{ site.url }}/artificial_intelligence/4.docx)*

Here is sample code of main loop:


{% highlight java linenos %}
 public void loop(){
				nacitajsubor();
				int k;
				while(true){  // v nekonecnej slucne sa najskor    otestuju vsetky pravidla, vytvoria sa tym padom instancie, potom sa odfiltruju 
				instancia.clear(); // a ak prejdu testom konca(test ci existuje nejaka instancia, ak nie tak ak existuje pravidlo hodne na opytanie sa tak sa opytaj)
				instanciaf.clear();	 // tak sa vykona prva instancia prveho pravidla
				for(int i=0;i<pravidlo.size();i++){ 					
					f(pravidlo.get(i),0,new Mapovanie()); }
				filter(); 
				if( (k = testkonca()) == 1 ){
					System.out.println("KONEC"); break;
				}
				if( k == 2 )
					continue;
				vykonaj(instanciaf.get(0));
				
				//vipis(instanciaf.get(0),0);
				}
			}
{% endhighlight %}
