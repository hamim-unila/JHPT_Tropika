# JHPT_Tropika
Mendeley style for JHPT Tropika
<?xml version="1.0" encoding="utf-8"?>
<style xmlns="http://purl.org/net/xbiblio/csl" class="in-text" version="1.0" demote-non-dropping-particle="never" default-locale="en-US">
  <!-- Comment start and end with -->
  <info>
    <title>0-Jurnal HPT Tropika Dec 2015 Updated-Hamim Sudarsono</title>
    <id>http://csl.mendeley.com/styles/4677531/0-Jurnal HPT Tropika Dec 2015 Updated-Hamim Sudarsono</id>
    <link href="http://www.zotero.org/styles/natureza-e-conservacao" rel="self"/>
    <link href="http://www.abeco.org.br/publicacoes/natureza-e-conservacao" rel="documentation"/>
    <author>
      <name>Mario JosÃ©</name>
      <email>gnumario [at-mark] gmail [dot-mark] com</email>
    </author>
    <contributor>
      <name>Hamim Sudarsono</name>
      <uri>http://www.mendeley.com/profiles/hamim-sudarsono/</uri>
    </contributor>
    <category citation-format="author-date"/>
    <category field="biology"/>
    <issn>1679-0073</issn>
    <eissn>2178-3675</eissn>
    <summary>Brazilian Journal of Nature Conservation</summary>
    <updated>2013-12-02T03:50:45+00:00</updated>
    <rights license="http://creativecommons.org/licenses/by-sa/3.0/">This work is licensed under a Creative Commons Attribution-ShareAlike 3.0 License</rights>
  </info>
  <locale xml:lang="en-US">
    <terms>
      <term name="month-01" form="short">jan.</term>
      <term name="month-02" form="short">feb.</term>
      <term name="month-03" form="short">mar.</term>
      <term name="month-04" form="short">apr.</term>
      <term name="month-05" form="short">may</term>
      <term name="month-06" form="short">jun.</term>
      <term name="month-07" form="short">jul.</term>
      <term name="month-08" form="short">aug.</term>
      <term name="month-09" form="short">sep.</term>
      <term name="month-10" form="short">oct.</term>
      <term name="month-11" form="short">nov.</term>
      <term name="month-12" form="short">dec.</term>
      <term name="editor" form="short">
        <single>ed.</single>
        <multiple>eds.</multiple>
      </term>
      <term name="container-author" form="short">
        <single>ed.</single>
        <multiple>eds.</multiple>
      </term>
      <term name="collection-editor" form="short">
        <single>ed.</single>
        <multiple>eds.</multiple>
      </term>
    </terms>
  </locale>
  <macro name="container">
    <choose>
      <if type="chapter paper-conference" match="any">
        <text value="In " font-style="italic"/>
        <names variable="container-author" delimiter=", ">
          <name sort-separator=", " initialize-with="" delimiter=" " delimiter-precedes-last="never" and="symbol">
            <name-part name="given" text-case="capitalize-first"/>
            <name-part name="family" text-case="capitalize-first"/>
          </name>
          <et-al font-style="italic"/>
          <label form="short" prefix=" (" suffix=")" text-case="lowercase"/>
          <substitute>
            <names variable="editor"/>
            <names variable="collection-editor"/>
          </substitute>
        </names>
        <text variable="container-title" suffix=". " prefix=", " font-style="italic"/>
      </if>
    </choose>
  </macro>
  <macro name="secondary-contributors">
    <choose>
      <if type="chapter" match="none">
        <names variable="editor" delimiter=", " prefix=" ">
          <name and="symbol" initialize-with="" delimiter=", "/>
          <label form="short" prefix=", " text-case="capitalize-first" suffix="."/>
        </names>
      </if>
    </choose>
  </macro>
  <macro name="author">
    <names variable="author">
      <name and="symbol" delimiter-precedes-last="never" initialize-with="" name-as-sort-order="all" sort-separator=" ">
        <name-part name="family" text-case="capitalize-first"/>
        <name-part name="given" text-case="capitalize-first"/>
      </name>
      <et-al font-style="italic"/>
      <label form="short" prefix=" (" suffix=".)" text-case="capitalize-first"/>
      <substitute>
        <names variable="editor"/>
        <names variable="translator"/>
        <text macro="title"/>
      </substitute>
    </names>
  </macro>
  <macro name="author-short">
    <names variable="author">
      <name form="short" name-as-sort-order="all" sort-separator=" " initialize-with="" delimiter="; " delimiter-precedes-last="never" and="symbol">
        <name-part name="family" text-case="capitalize-first"/>
        <name-part name="given" text-case="capitalize-first"/>
      </name>
      <et-al font-style="italic"/>
      <substitute>
        <names variable="editor"/>
        <names variable="translator"/>
        <choose>
          <if type="book">
            <text variable="title" form="short"/>
          </if>
          <else>
            <text variable="title" form="short" quotes="true"/>
          </else>
        </choose>
      </substitute>
    </names>
  </macro>
  <macro name="access">
    <text variable="URL" prefix=" Website: " suffix=""/>
    <date variable="accessed" prefix=" [Accessed: " suffix="].">
      <date-part name="day" suffix=" "/>
      <date-part name="month" suffix=" "/>
      <date-part name="year"/>
    </date>
  </macro>
  <macro name="title">
    <choose>
      <if type="book">
        <text variable="title" font-style="italic"/>
      </if>
      <else>
        <text variable="title"/>
      </else>
    </choose>
  </macro>
     <macro name="container-title">
    <text variable="container-title" font-style="italic"/>
     </macro>
  <macro name="publisher">
    <group delimiter=", ">
	   <text variable="publisher"/>
      <text variable="publisher-place" suffix=""/>
    </group>
	<group delimiter="">
	  <text macro="access" prefix="." suffix=""/>
      <text variable="number-of-pages" prefix =". " suffix=" p."/>
    </group>
  </macro>
    <macro name="pages">
    <group>
      <text variable="page"/>
    </group>
   </macro>
  <macro name="issued-year">
    <choose>
      <if variable="issued" match="any">
        <date variable="issued">
          <date-part name="year"/>
        </date>
      </if>
    </choose>
  </macro>
  <macro name="edition">
    <choose>
      <if type="book chapter" match="any">
        <choose>
          <if is-numeric="edition">
            <group delimiter=" ">
              <number variable="edition" form="ordinal"/>
              <text term="edition" form="short" suffix="." prefix=" "/>
            </group>
          </if>
          <else>
            <text variable="edition" suffix=" ed."/>
          </else>
        </choose>
      </if>
    </choose>
  </macro>
  <macro name="locators">
    <choose>
      <if type="bill legislation" match="any">
        <group prefix=". " delimiter=", ">
          <date variable="issued">
            <date-part name="day"/>
            <date-part prefix=" " name="month" form="short"/>
            <date-part prefix=" " name="year"/>
          </date>
          <text variable="section" prefix="Sec. "/>
          <text variable="page" prefix=" " suffix="."/>
        </group>
      </if>
      <else-if match="any" type="article-journal article-magazine article-newspaper">
        <group>
          <text variable="volume" suffix=" "/>
          <text variable="issue" prefix="(" suffix=")"/>
          <text variable="page" prefix=": "/>
        </group>
      </else-if>
      <else-if match="any" type="book chapter">
        <group delimiter=", ">
          <text variable="volume" prefix="v. "/>
		  <text variable="page" prefix=" " suffix =" p"/>
		</group>
      </else-if>
    </choose>
  </macro>
  <macro name="citation-locator">
    <group>
      <label variable="locator" form="short"/>
      <text variable="locator" prefix=" "/>
    </group>
  </macro>
  <macro name="genre">
    <text variable="genre"/>
  </macro>
  <citation et-al-min="3" et-al-use-first="1" et-al-subsequent-min="3" et-al-subsequent-use-first="1" disambiguate-add-year-suffix="true" disambiguate-add-names="true" collapse="year">
    <sort>
      <key macro="author"/>
      <key variable="issued"/>
    </sort>
    <layout prefix="(" suffix=")" delimiter="; ">
      <group delimiter=",">
        <text macro="author-short"/>
        <text macro="issued-year" prefix=" "/>
        <text prefix=", " macro="citation-locator"/>
      </group>
    </layout>
  </citation>
  <bibliography et-al-min="18" et-al-use-first="18" hanging-indent="true">
    <sort>
      <key macro="author"/>
      <key variable="issued"/>
    </sort>
    <layout>
      <choose>
        <if type="bill legislation" match="any">
          <text macro="author" suffix=". "/>
          <text variable="number" suffix=". "/>
          <text macro="title" suffix=". "/>
          <text variable="references" suffix=", "/>
          <text variable="note"/>
          <text macro="locators" suffix=". "/>
        </if>
		
        <else-if type="map">
          <text macro="author" suffix=", "/>
          <text macro="issued-year" suffix=". "/>
          <group suffix=". " delimiter=", ">
            <text macro="title"/>
            <text variable="note"/>
          </group>
        </else-if>
		
        <else-if type="book">
          <text macro="author" suffix=". "/>
          <text macro="issued-year" suffix=". "/>
          <text macro="title" suffix=". "/>
          <group delimiter=" " suffix=".">
            <text macro="edition"/>
            <text macro="publisher"/>
 		 </group>	
         </else-if>
		
        <else-if type="chapter">
          <text macro="author" suffix=".  "/>
          <text macro="issued-year" suffix=". "/>
          <text macro="title" suffix=". "/>
          <text macro="container" suffix=" "/>
          <text macro="secondary-contributors" suffix=". "/>
          <text variable="collection-title" suffix=". "/>
          <group suffix="." delimiter=". ">
            <text macro="edition"/>
            <text macro="publisher"/>
            <text macro="locators"/>
          </group>
        </else-if>
        <else-if type="article-newspaper article-magazine article-journal" match="any">
          <text macro="author" suffix=". "/>
          <text macro="issued-year" suffix=". "/>
          <text macro="title" suffix=". "/>
          <text macro="container-title" suffix=", "/>
          <text variable="collection-title" suffix=". "/>
          <group suffix=". " delimiter=", ">
            <text macro="edition"/>
            <text macro="locators"/>
          </group>
        </else-if>


		<if type="thesis">
          <text macro="author" suffix=". "/>
          <text macro="issued-year" suffix=". "/>
          <text macro="title" suffix=". "/>  
  	  	  <text macro="publisher"/>  
		</if>
<!-- Comment start and end with -->
        <else-if type="thesis">
          <text macro="author" suffix=". "/>
          <text macro="issued-year" suffix=". "/>
          <text macro="title" suffix=". "/>
       	  <text macro="container-title" suffix=". "/>
		  <text prefix=" " suffix="." macro="publisher"/>
		  <text macro="access" suffix="."/>
        </else-if>
		
		
        <else-if type="webpage report">
          <text macro="author" suffix=". "/>
		  <text macro="issued-year" suffix=". "/>
          <text macro="title" suffix=". "/>
		  <text macro="container-title" suffix=""/>
		  <text macro="publisher"/>

        </else-if>
        <else>
          <text macro="author" suffix=". "/>
          <text macro="issued-year" suffix=". "/>
          <text macro="title" suffix=". "/>
          <text macro="container"/>
          <text macro="secondary-contributors"/>
          <text macro="container-title" suffix=". "/>
          <text variable="collection-title" prefix="," suffix="."/>
          <text macro="publisher" suffix="."/>
          <text macro="locators" suffix="."/>
        </else>
      </choose>
    </layout>
  </bibliography>
</style>
