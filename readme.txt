--------------------
Modul til visning af fredede og bevaringsværdige bygninger og fund & fortidsminder fra Kulturstyrelsen
-------------------- 

INSTALLATION :

1:   Installér modulet
1.a: Kopiér modulet "kust" til sitets moduler, dvs. til "[cbinfo.config.dir]/modules/custom/kust"
1.b: Skriv følgende entry i [cbinfo.modules]: <module name="kust" dir="custom/kust" permissionlevel="public"/>

2:   Rediger Profil(er)
2.a: Tilføj et eller flere af temaerne til profilen.
2.b: Det kan evt. gøres vha. includes af hhv. temagruppe og temaer:
        <include mustexist="false" nodes="/profile/themegroups/*" src="[module:kust.dir]/profiles/profile.xml"/>
        <include mustexist="false" nodes="/profile/themes/*" src="[module:kust.dir]/profiles/profile.xml"/>
      
3:   Rediger targetsets
3.a: Tilføj det target, der findes skabelonen i targetset.xml under mappen "queries"
     hvor de mulige targets med tilhørende referencer til datasource, temafil og presentation.
     Det kan evt. tilføjes vha. include:
        <include src="[module:kust.dir]/queries/targetset.xml" nodes="/spatialqueries/targetset/*" mustexist="false"/>

4:	 Tilføj signatur
4.a: Billeder i /images kopieres til /resources/symbols/custom/images/

4.b: Følgende sættes ind i symbols5_6.txt:

SYMBOL
    NAME 'bygning_alle'
    TYPE PIXMAP
    IMAGE 'custom/images/bygning_alle.png'
END

SYMBOL
    NAME 'bygning_bevaringssag'
    TYPE PIXMAP
    IMAGE 'custom/images/bygning_bevaringssag.gif'
END

SYMBOL
    NAME 'bygning_hoej_bevaringsvaerdi'
    TYPE PIXMAP
    IMAGE 'custom/images/bygning_hoej_bevaringsvaerdi.gif'
END

SYMBOL
    NAME 'bygning_lav_bevaringsvaerdi'
    TYPE PIXMAP
    IMAGE 'custom/images/bygning_lav_bevaringsvaerdi.png'
END

SYMBOL
    NAME 'bygning_medium_bevaringsvaerdi'
    TYPE PIXMAP
    IMAGE 'custom/images/bygning_medium_bevaringsvaerdi.png'
END

SYMBOL
    NAME 'fredede_bygning'
    TYPE PIXMAP
    IMAGE 'custom/images/fredede_bygninger.gif'
END

SYMBOL
    NAME 'indkig'
    TYPE PIXMAP
    IMAGE 'custom/images/indkig.png'
END

SYMBOL
    NAME 'udsigt'
    TYPE PIXMAP
    IMAGE 'custom/images/udsigt.png'
END		
		
AFHÆNGIGHEDER: 

CBkort 2.6 eller nyere.

VERSIONSHISTORIK

29-11-2012

Modulerne "kust" og "fbb" er lagt sammen, da alle datasættene udstilles fra samme styrelse (Kulturstyrelsen). Endvidere er tilføjet signaturforklaring til lagene fra fredede og bevaringsværdige bygninger. Der er pt. stadig problemer med print af fredede & bevaringsværdige bygninger fra den udstillede WMS service

13-5-2013

Presentations indeholder nu (dybe) links til Kulturstyrelsens site med fredede & bevaringsværdige bygninger. Endvidere er tilføjet en række nye temaer (SAVE) til modulet ("Bebygget struktur").

