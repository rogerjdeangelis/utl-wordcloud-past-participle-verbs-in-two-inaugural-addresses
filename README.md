# utl-wordcloud-past-participle-verbs-in-two-inaugural-addresses
Wordcloud past participle verbs in two inaugural addresses
    %let pgm=utl-wordcloud-past-participle-verbs-in-two-inaugural-addresses;

    %stop_submission;

    Wordcloud past participle verbs in two inaugural addresses

      CONTENTS

          1 wordcloud after prep (2 & 3 create the inputs for the wordcloud)
          2 prep for president 1 (see below)
          3 prep for president 2 (see below)

    Graphic output
    https://tinyurl.com/42zyttre
    https://github.com/rogerjdeangelis/utl-wordcloud-past-participle-verbs-in-two-inaugural-addresses/blob/main/pres1.png

    https://tinyurl.com/mmm82fj9
    https://github.com/rogerjdeangelis/utl-wordcloud-past-participle-verbs-in-two-inaugural-addresses/blob/main/pres2.png
                                                      U
    github
    https://tinyurl.com/4wtede9h
    https://github.com/rogerjdeangelis/utl-wordcloud-past-participle-verbs-in-two-inaugural-addresses

    Html versions
    https://github.com/rogerjdeangelis/utl-wordcloud-past-participle-verbs-in-two-inaugural-addresses/blob/main/pres2.html
    https://github.com/rogerjdeangelis/utl-wordcloud-past-participle-verbs-in-two-inaugural-addresses/blob/main/pres1.html


    /**************************************************************************************************************************/
    /*         INPUT                              |   PROCESS                       |  OUTPUT                                 */
    /*         =====                              |   =======                       |  ======                                 */
    /*                                            |                                 |                                         */
    /*  Verb,                                     | 1 WORDCLOUD AFTER PREP          |                                         */
    /*  past                                      | =====================           | president 1                             */
    /*  participle                                |                                 | https://tinyurl.com/42zyttre            */
    /*                                            | %utl_rbeginx;                   |                                         */
    /*      Pesident 1          President 2       | parmcards4;                     | president 2                             */
    /*                                            | library(haven);                 | https://tinyurl.com/mmm82fj9            */
    /*  CAT         COUNT    CAT       COUNT      | library(wordcloud2);            |                                         */
    /*                                            | library(htmlwidgets);           |                                         */
    /*  ourcreed      4      broken      6        | library(haven)                  |                                         */
    /*  created       2      spent       6        | library(webshot)                |                                         */
    /*  drawn         2      treated     6        | tmp_file <-                     |                                         */
    /*  sworn         2      built       4        |   tempfile(fileext=".html")     |                                         */
    /*  articulated   1      given       4        | have<-read_sas(                 |                                         */
    /*  begun         1      respected   4        |  "d:/sd1/pres1.sas7bdat")       |                                         */
    /*  born          1      saved       4        | my_graph<-wordcloud2(           |                                         */
    /*  bound         1      seen        4        |   data = have)                  |                                         */
    /*  cared         1      shown       4        | saveWidget(                     |                                         */
    /*  cured         1      taken       4        |    my_graph                     |                                         */
    /*                                            |   ,tmp_file                     |                                         */
    /*                                            |   ,selfcontained = F)           |                                         */
    /* options validvarname=upcase;               | webshot(tmp_file                |                                         */
    /* libname sd1 "d:/sd1";                      |   ,"d:/png/pres1.png"           |                                         */
    /* data sd1.have;                             |   ,delay=5,vwidth=800           |                                         */
    /*                                            |   ,vheight=800)                 |                                         */
    /* data sd1.pres1;      data sd1.pres2;       |                                 |                                         */
    /* retain cat;          retain cat;           | have<-read_sas(                 |                                         */
    /*  input                input                |  "d:/sd1/pres2.sas7bdat")       |                                         */
    /*   count                count               | my_graph<-wordcloud2(           |                                         */
    /*    cat $16.;            cat $16.;          |   data = have)                  |                                         */
    /* cards4;              cards4;               | saveWidget(                     |                                         */
    /* 4 ourcreed           6 broken              |    my_graph                     |                                         */
    /* 2 created            6 spent               |   ,tmp_file                     |                                         */
    /* 2 drawn              6 treated             |   ,selfcontained = F)           |                                         */
    /* 2 sworn              4 built               | webshot(tmp_file                |                                         */
    /* 1 articulated        4 given               |   ,"d:/png/pres2.png"           |                                         */
    /* 1 begun              4 respected           |   ,delay=5,vwidth=800           |                                         */
    /* 1 born               4 saved               |   ,vheight=800)                 |                                         */
    /* 1 bound              4 seen                | ;;;;                            |                                         */
    /* 1 cared              4 shown               | %utl_rendx;                     |                                         */
    /* 1 cured              4 taken               |                                 |                                         */
    /* ;;;;                 ;;;;                  |                                 |                                         */
    /* run;quit;            run;quit;             | 2 PREP FOR PRESIDENT 1          |                                         */
    /*                                            | ======================          |                                         */
    /*                                            |                                 |                                         */
    /*                                            | see below                       |                                         */
    /*                                            |                                 |                                         */
    /*                                            |                                 |                                         */
    /*                                            | 3 PREP FOR PRESIDENT 2          |                                         */
    /*                                            | ======================          |                                         */
    /*                                            |                                 |                                         */
    /*                                            | see below                       |                                         */
    /**************************************************************************************************************************/

    /*                   _
    (_)_ __  _ __  _   _| |_
    | | `_ \| `_ \| | | | __|
    | | | | | |_) | |_| | |_
    |_|_| |_| .__/ \__,_|\__|
            |_|
    */

    data sd1.pres1;
    retain cat;
     input
      count
       cat $16.;
    cards4;
    4 ourcreed
    2 created
    2 drawn
    2 sworn
    1 articulated
    1 begun
    1 born
    1 bound
    1 cared
    1 cured
    ;;;;
    run;quit;

    data sd1.pres2;
    retain cat;
     input
      count
       cat $16.;
    cards4;
    6 broken
    6 spent
    6 treated
    4 built
    4 given
    4 respected
    4 saved
    4 seen
    4 shown
    4 taken
    ;;;;
    run;quit;

    /**************************************************************************************************************************/
    /*       Pesident 1          President 2                                                                                  */
    /*                                                                                                                        */
    /*   CAT         COUNT    CAT       COUNT                                                                                 */
    /*                                                                                                                        */
    /*   ourcreed      4      broken      6                                                                                   */
    /*   created       2      spent       6                                                                                   */
    /*   drawn         2      treated     6                                                                                   */
    /*   sworn         2      built       4                                                                                   */
    /*   articulated   1      given       4                                                                                   */
    /*   begun         1      respected   4                                                                                   */
    /*   born          1      saved       4                                                                                   */
    /*   bound         1      seen        4                                                                                   */
    /*   cared         1      shown       4                                                                                   */
    /*   cured         1      taken       4                                                                                   */
    /**************************************************************************************************************************/

    /*                         _      _                 _          __ _
    / | __      _____  _ __ __| | ___| | ___  _   _  __| |   __ _ / _| |_ ___ _ __  _ __  _ __ ___ _ __
    | | \ \ /\ / / _ \| `__/ _` |/ __| |/ _ \| | | |/ _` |  / _` | |_| __/ _ \ `__|| `_ \| `__/ _ \ `_ \
    | |  \ V  V / (_) | | | (_| | (__| | (_) | |_| | (_| | | (_| |  _| ||  __/ |   | |_) | | |  __/ |_) |
    |_|   \_/\_/ \___/|_|  \__,_|\___|_|\___/ \__,_|\__,_|  \__,_|_|  \__\___|_|   | .__/|_|  \___| .__/
     _                                                                             |_|            |_|
    (_)_ __  _ __  _   _| |_
    | | `_ \| `_ \| | | | __|
    | | | | | |_) | |_| | |_
    |_|_| |_| .__/ \__,_|\__|
            |_|
    */

    %utl_rbeginx;
    parmcards4;
    library(haven);
    library(wordcloud2);
    library(htmlwidgets);
    library(haven)
    library(webshot)
    tmp_file <-
      tempfile(fileext=".html")
    have<-read_sas(
     "d:/sd1/pres1.sas7bdat")
    my_graph<-wordcloud2(
      data = have)
    saveWidget(
       my_graph
      ,tmp_file
      ,selfcontained = F)
    webshot(tmp_file
      ,"d:/png/pres1.png"
      ,delay=5,vwidth=800
      ,vheight=800)

    have<-read_sas(
     "d:/sd1/pres2.sas7bdat")
    my_graph<-wordcloud2(
      data = have)
    saveWidget(
       my_graph
      ,tmp_file
      ,selfcontained = F)
    webshot(tmp_file
      ,"d:/png/pres2.png"
      ,delay=5,vwidth=800
      ,vheight=800)
    ;;;;
    %utl_rendx;

    /**************************************************************************************************************************/
    /* Predident 1                                                                                                            */
    /* https://tinyurl.com/42zyttre                                                                                           */
    /* https://github.com/rogerjdeangelis/utl-wordcloud-past-participle-verbs-in-two-inaugural-addresses/blob/main/pres1.png  */
    /*                                                                                                                        */
    /* Predident 2                                                                                                            */
    /* https://tinyurl.com/mmm82fj9                                                                                           */
    /* https://github.com/rogerjdeangelis/utl-wordcloud-past-participle-verbs-in-two-inaugural-addresses/blob/main/pres2.png  */
    /**************************************************************************************************************************/

    /*___                                               _     _            _    _
    |___ \   _ __  _ __ ___ _ __    _ __  _ __ ___  ___(_) __| | ___ _ __ | |_ / |
      __) | | `_ \| `__/ _ \ `_ \  | `_ \| `__/ _ \/ __| |/ _` |/ _ \ `_ \| __|| |
     / __/  | |_) | | |  __/ |_) | | |_) | | |  __/\__ \ | (_| |  __/ | | | |_ | |
    |_____| | .__/|_|  \___| .__/  | .__/|_|  \___||___/_|\__,_|\___|_| |_|\__||_|
            |_|            |_|     |_|
    */

    proc datasets lib=sd1 nolist nodetails;
     delete apassage;
    run;quit;

    options validvarname=upcase lrecl=255;
    libname sd1 "d:/sd1";
    data sd1.apassage(drop=infile) ;
    length  infile $115 passage $32756.;
    retain passage;
    infile cards4 eof=at_end;
    input infile &;
     infile = compress(infile,, 'dp');
     passage=catx(' ',passage,infile);
     return;
     at_end:
       output;
    cards4;
    Vice President Biden, Mr. Chief Justice, members of the United States Congress, distinguished guests, and
    fellow citizens, each time we gather to inaugurate a president, we bear witness to the enduring strength of
    our Constitution. We affirm the promise of our democracy. We recall that what binds this nation together is
    not the colors of our skin or the tenets of our faith or the origins of our names.  What makes us exceptional,
    what makes us America is our allegiance to an idea articulated in a declaration made more than two centuries
    ago:  We hold these truths to be self-evident, that all men are created equal, that they are endowed by their
    Creator with certain unalienable Rights, that among these are Life, Liberty and the pursuit of Happiness.
    Today we continue a never ending journey to bridge the meaning of those words with the realities of our time.
    For history tells us that while these truths may be self-evident, they’ve never been self-executing. That
    while freedom is a gift from God, it must be secured by his people here on earth.  The patriots of 1776 did
    not fight to replace the tyranny of a king with the privileges of a few, or the rule of a mob. They gave to us
    a republic, a government of, and by, and for the people. Entrusting each generation to keep safe our founding
    creed. And for more than 200 years we have. Through blood drawn by lash, and blood drawn by sword, we noted
    that no union founded on the principles of liberty and equality could survive half slave, and half free. We
    made ourselves anew, and vowed to move forward together.  Together we determined that a modern economy
    requires railroads and highways to speed travel and commerce, schools and colleges to train our workers.
    Together we discovered that a free market only thrives when there are rules to ensure competition and fair
    play. Together we resolve that a great nation must care for the vulnerable and protect its people from life’s
    worst hazards and misfortune.  Through it all, we have never relinquished our skepticism of central authority,
    nor have we succumbed to the fiction that all societies ills can be cured through government alone. Our
    celebration of initiative and enterprise, our insistence on hard work and personal responsibility, these are
    constants in our character.  But we have always understood that when times change, so must we; that fidelity
    to our founding principles requires new responses to new challenges; that preserving our individual freedoms
    ultimately requires collective action. For the American people can no more meet the demands of today’s world
    by acting alone than American soldiers could have met the forces of fascism or communism with muskets and
    militias. No single person can train all the math and science teachers we’ll need to equip our children for
    the future, or build the roads and networks and research labs that will bring new jobs and businesses to our
    shores. Now, more than ever, we must do these things together, as one nation and one people.  This generation
    of Americans has been tested by crises that steeled our resolve and proved our resilience.  A decade of war is
    now ending. An economic recovery has begun. America’s possibilities are limitless, for we possess all the
    qualities that this world without boundaries demands:  youth and drive; diversity and openness; an endless
    capacity for risk and a gift for reinvention. My fellow Americans, we are made for this moment, and we will
    seize it -- so long as we seize it together.  For we, the people, understand that our country cannot succeed
    when a shrinking few do very well and a growing many barely make it. We believe that America’s prosperity must
    rest upon the broad shoulders of a rising middle class. We know that America thrives when every person can
    find independence and pride in their work; when the wages of honest labor liberate families from the brink of
    hardship. We are true to our creed when a little girl born into the bleakest poverty knows that she has the
    same chance to succeed as anybody else, because she is an American; she is free, and she is equal, not just in
    the eyes of God but also in our own.  We understand that outworn programs are inadequate to the needs of our
    time. So we must harness new ideas and technology to remake our government, revamp our tax code, reform our
    schools, and empower our citizens with the skills they need to work harder, learn more, reach higher. But
    while the means will change, our purpose endures. A nation that rewards the effort and determination of every
    single American. That is what this moment requires. That is what will give real meaning to our creed.  We, the
    people, still believe that every citizen deserves a basic measure of security and dignity. We must make the
    hard choices to reduce the cost of health care and the size of our deficit. But we reject the belief that
    America must choose between caring for the generation that built this country and investing in the generation
    that will build its future. For we remember the lessons of our past, when twilight years were spent in poverty
    and parents of a child with a disability had nowhere to turn.  We do not believe that in this country freedom
    is reserved for the lucky, or happiness for the few. We recognize that no matter how responsibly we live our
    lives, any one of us at any time may face a job loss, or a sudden illness, or a home swept away in a terrible
    storm. The commitments we make to each other through Medicare and Medicaid and Social Security, these things
    do not sap our initiative, they strengthen us. They do not make us a nation of takers; they free us to take
    the risks that make this country great.  We, the people, still believe that our obligations as Americans are
    not just to ourselves, but to all posterity. We will respond to the threat of climate change, knowing that the
    failure to do so would betray our children and future generations. Some may still deny the overwhelming
    judgment of science, but none can avoid the devastating impact of raging fires and crippling drought and more
    powerful storms.  The path towards sustainable energy sources will be long and sometimes difficult. But
    America cannot resist this transition, we must lead it. We cannot cede to other nations the technology that
    will power new jobs and new industries, we must claim its promise. That’s how we will maintain our economic
    vitality and our national treasure -- our forests and waterways, our crop lands, and snow-capped peaks. That
    is how we will preserve our planet, commanded to our care by God. That’s what will lend meaning to the creed
    our Fathers once declared.  We, the people, still believe that enduring security and lasting peace do not
    require perpetual war. Our brave men and women in uniform, tempered by the flames of battle, are unmatched in
    skill and courage. Our citizens, seared by the memory of those we have lost, know too well the price that is
    paid for liberty. The knowledge of their sacrifice will keep us forever vigilant against those who would do us
    harm. But we are also heirs to those who won the peace and not just the war; who turned sworn enemies into the
    surest of friends -- and we must carry those lessons into this time as well.  We will defend our people and
    uphold our values through strength of arms and rule of law. We will show the courage to try and resolve our
    differences with other nations peacefully -- not because we are naïve about the dangers we face, but because
    engagement can more durably lift suspicion and fear.  America will remain the anchor of strong alliances in
    every corner of the globe. And we will renew those institutions that extend our capacity to manage crisis
    abroad, for no one has a greater stake in a peaceful world than its most powerful nation. We will support
    democracy from Asia to Africa, from the Americas to the Middle East, because our interests and our conscience
    compel us to act on behalf of those who long for freedom. And we must be a source of hope to the poor, the
    sick, the marginalized, the victims of prejudice -- not out of mere charity, but because peace in our time
    requires the constant advance of those principles that our common creed describes: tolerance and opportunity,
    human dignity, and justice.  We, the people, declare today that the most evident of truths -- that all of us
    are created equal -- is the star that guides us still; just as it guided our forebears through Seneca Falls,
    and Selma, and Stonewall; just as it guided all those men and women, sung and unsung, who left footprints
    along this great Mall, to hear a preacher say that we cannot walk alone; to hear a "King" proclaim that our
    individual freedom is inextricably bound to the freedom of every soul on Earth.  It is now our generation’s
    task to carry on what those pioneers began. For our journey is not complete until our wives, our mothers and
    daughters can earn a living equal to their efforts.  Our journey is not complete until our gay brothers and
    sisters are treated like anyone else under the law -- for if we are truly created equal, then surely the love
    we commit to one another must be equal as well.  Our journey is not complete until no citizen is forced to
    wait for hours to exercise the right to vote.  Our journey is not complete until we find a better way to
    welcome the striving, hopeful immigrants who still see America as a land of opportunity -- until bright young
    students and engineers are enlisted in our workforce rather than expelled from our country.  Our journey is
    not complete until all our children, from the streets of Detroit to the hills of Appalachia, to the quiet
    lanes of Newtown, know that they are cared for and cherished and always safe from harm.  That is our
    generation’s task: to make these words, these rights, these values of life and liberty and the pursuit of
    happiness real for every American. Being true to our founding documents does not require us to agree on every
    contour of life. It does not mean we all define liberty in exactly the same way or follow the same precise
    path to happiness. Progress does not compel us to settle centuries-long debates about the role of government
    for all time, but it does require us to act in our time.  For now decisions are upon us and we cannot afford
    delay. We cannot mistake absolutism for principle, or substitute spectacle for politics, or treat name-calling
    as reasoned debate. We must act, knowing that our work will be imperfect. We must act, knowing that today’s
    victories will be only partial and that it will be up to those who stand here in four years and 40 years and
    400 years hence to advance the timeless spirit once conferred to us in a spare Philadelphia hall.  My fellow
    Americans, the oath I have sworn before you today, like the one recited by others who serve in this Capitol,
    was an oath to God and country, not party or faction.  And we must faithfully execute that pledge during the
    duration of our service. But the words I spoke today are not so different from the oath that is taken each
    time a soldier signs up for duty or an immigrant realizes her dream. My oath is not so different from the
    pledge we all make to the flag that waves above and that fills our hearts with pride.  They are the words of
    citizens and they represent our greatest hope. You and I, as citizens, have the power to set this country’s
    course. You and I, as citizens, have the obligation to shape the debates of our time -- not only with the
    votes we cast, but with the voices we lift in defense of our most ancient values and enduring ideals.  Let us,
    each of us, now embrace with solemn duty and awesome joy what is our lasting birthright. With common effort
    and common purpose, with passion and dedication, let us answer the call of history and carry into an uncertain
    future that precious light of freedom.
    ;;;;;
    run;quit;

    proc format;
     value $tok2grammer
      "CC  "="Coordinating conjunction                "
      "CD  "="Cardinal number                         "
      "DT  "="Determiner                              "
      "EX  "="Existential there                       "
      "FW  "="Foreign word                            "
      "IN  "="Preposition or subordinating conjunction"
      "JJ  "="Adjective                               "
      "JJR "="Adjective, comparative                  "
      "JJS "="Adjective, superlative                  "
      "LS  "="List item marker                        "
      "MD  "="Modal                                   "
      "NN  "="Noun, singular or mass                  "
      "NNS "="Noun, plural                            "
      "NNP "="Proper noun, singular                   "
      "NNPS"="Proper noun, plural                     "
      "PDT "="Predeterminer                           "
      "POS "="Possessive ending                       "
      "PRP "="Personal pronoun                        "
      "PRP$"="Possessive pronoun                      "
      "RB  "="Adverb                                  "
      "RBR "="Adverb, comparative                     "
      "RBS "="Adverb, superlative                     "
      "RP  "="Particle                                "
      "SYM "="Symbol                                  "
      "UH  "="Interjection                            "
      "VB  "="Verb, base form                         "
      "VBD "="Verb, past tense                        "
      "VBG "="Verb, gerund or present participle      "
      "VBN "="Verb, past participle                   "
      "VBP "="Verb, non­3rd person singular present   "
      "VBZ "="Verb, 3rd person singular present       "
      "WDT "="Wh­determiner                           "
      "WP  "="Wh­pronoun                              "
      "WP$ "="Possessive wh­pronoun                   "
      "WRB "="Wh­adverb                               "
      other="Preposition"
    ;run;quit;

    /*
     _ __  _ __ ___   ___ ___  ___ ___
    | `_ \| `__/ _ \ / __/ _ \/ __/ __|
    | |_) | | | (_) | (_|  __/\__ \__ \
    | .__/|_|  \___/ \___\___||___/___/
    |_|
    */

    proc datasets lib=sd1 nolist nodetails;
     delete awant;
    run;quit;

    %utl_rbeginx;
    parmcards4;
    library(stringr)
    library(NLP)
    library(openNLP)
    library(haven)
    source("c:/oto/fn_tosas9x.R")
    txt<-read_sas("d:/sd1/apassage.sas7bdat")
    s <- as.String(txt$PASSAGE)
    sent_token_annotator<-
      Maxent_Sent_Token_Annotator()
    word_token_annotator <-
      Maxent_Word_Token_Annotator()
    a2 <- annotate(s
     ,list(sent_token_annotator
     ,word_token_annotator))
    pos_tag_annotator <-
      Maxent_POS_Tag_Annotator()
    pos_tag_annotator
    a3 <- annotate(s
      ,pos_tag_annotator
      ,a2)
    head(annotate(s
     ,Maxent_POS_Tag_Annotator(probs=TRUE)
     ,a2))
    a3w <- subset(a3, type == "word")
    tags <- sapply(a3w$features,`[[`,"POS")
    want<-as.data.frame(sprintf("%s/%s"
     ,s[a3w], tags))
    colnames(want)<-"wrdGrm"
    fn_tosas9x(
          inp    = want
         ,outlib ="d:/sd1/"
         ,outdsn ="awant"
         )
    ;;;;
    %utl_rendx;

    /**************************************************************************************************************************/
    /* SD1.AWANT total obs=1,831                                                                                              */
    /*  ROWNAMES    WRDGRM                                                                                                    */
    /*                                                                                                                        */
    /*      1       Vice/NNP                                                                                                  */
    /*      2       President/NNP                                                                                             */
    /*      3       Biden/NNP                                                                                                 */
    /*      4       Mr/NNP                                                                                                    */
    /*      5       Chief/NNP                                                                                                 */
    /*   ...                                                                                                                  */
    /*   1827       that/IN                                                                                                   */
    /*   1828       precious/JJ                                                                                               */
    /*   1829       light/NN                                                                                                  */
    /*   1830       of/IN                                                                                                     */
    /*   1831       freedom/NN                                                                                                */
    /**************************************************************************************************************************/

    data atemp ;
      set sd1.awant;
      word=scan(wrdGrm,1,'/');
      grm=scan(wrdGrm,2,'/');
      grammer=put(strip(grm)
      ,$tok2grammer.);
      if grammer=:"Verb, past participle";
      if word ="been" then delete;
       keep word grammer;
    run;quit;

    /**************************************************************************************************************************/
    /* ATEMP total obs=37                                                                                                     */
    /* Obs    WORD                  GRAMMER                                                                                   */
    /*                                                                                                                        */
    /*   Obs    WORD                   GRAMMER                                                                                */
    /*                                                                                                                        */
    /*     1    articulated     Verb, past participle                                                                         */
    /*     2    created         Verb, past participle                                                                         */
    /*     3    secured         Verb, past participle                                                                         */
    /*     4    drawn           Verb, past participle...                                                                      */
    /*     ...                                                                                                                */
    /*    34    reasoned       Verb, past participle                                                                          */
    /*    35    sworn          Verb, past participle                                                                          */
    /*    36    recited        Verb, past participle                                                                          */
    /*    37    taken          Verb, past participle                                                                          */
    /**************************************************************************************************************************/

    proc freq data=atemp order=freq;
     tables word / list out=sd1.pres1
        (keep=word count rename=word=cat);
    run;quit;

    /**************************************************************************************************************************/
    /* SD1.PRES1 total obs=31                                                                                                 */
    /* Obs    CAT            COUNT                                                                                            */
    /*                                                                                                                        */
    /*   1    creed            4                                                                                              */
    /*   2    created          2                                                                                              */
    /*   3    drawn            2                                                                                              */
    /*   4    sworn            2                                                                                              */
    /*   5    articulated      1                                                                                              */
    /*   6    begun            1                                                                                              */
    /*   7    born             1                                                                                              */
    /*   8    bound            1                                                                                              */
    /*   9    cared            1                                                                                              */
    /*  10    cured            1                                                                                              */
    /*  11    enlisted         1                                                                                              */
    /*  12    expelled         1                                                                                              */
    /*  13    lost             1                                                                                              */
    /*  14    made             1                                                                                              */
    /*  15    met              1                                                                                              */
    /*  16    paid             1                                                                                              */
    /*  17    reasoned         1                                                                                              */
    /*  18    recited          1                                                                                              */
    /*  19    reserved         1                                                                                              */
    /*  20    seared           1                                                                                              */
    /*  21    secured          1                                                                                              */
    /*  22    spent            1                                                                                              */
    /*  23    succumbed        1                                                                                              */
    /*  24    sung             1                                                                                              */
    /*  25    swept            1                                                                                              */
    /*  26    taken            1                                                                                              */
    /*  27    tempered         1                                                                                              */
    /*  28    tested           1                                                                                              */
    /*  29    treated          1                                                                                              */
    /*  30    unmatched        1                                                                                              */
    /*  31    uphold           1                                                                                              */
    /**************************************************************************************************************************/

    /*____                                              _     _            _    ____
    |___ /   _ __  _ __ ___ _ __    _ __  _ __ ___  ___(_) __| | ___ _ __ | |_ |___ \
      |_ \  | `_ \| `__/ _ \ `_ \  | `_ \| `__/ _ \/ __| |/ _` |/ _ \ `_ \| __|  __) |
     ___) | | |_) | | |  __/ |_) | | |_) | | |  __/\__ \ | (_| |  __/ | | | |_  / __/
    |____/  | .__/|_|  \___| .__/  | .__/|_|  \___||___/_|\__,_|\___|_| |_|\__||_____|
            |_|            |_|     |_|
    */

    proc datasets lib=sd1 nolist nodetails;
     delete bpassage;
    run;quit;

    options validvarname=upcase lrecl=255;
    libname sd1 "d:/sd1";
    data sd1.bpassage(drop=infile) ;
    length  infile $115 passage $32756.;
    retain passage;
    infile cards4 eof=at_end;
    input infile &;
     infile = compress(infile,, 'dp');
     passage=catx(' ',passage,infile);
     return;
     at_end:
       output;
    cards4;
    The golden age of America begins right now. From this day forward, our country will flourish and be respected
    again all over the world. We will be the envy of every nation, and we will not allow ourselves to be taken
    advantage of any longer. During every single day of the Trump Administration, I will, very simply, put America
    first. Our sovereignty will be reclaimed. Our safety will be restored. The scales of justice will be
    rebalanced. The vicious, violent, and unfair weaponization of the Justice Department and our government will
    end. And our top priority will be to create a nation that is proud, prosperous, and free. America will soon
    be greater, stronger, and far more exceptional than ever before. I return to the presidency confident and
    optimistic that we are at the start of a thrilling new era of national success. A tide of change is sweeping
    the country, sunlight is pouring over the entire world, and America has the chance to seize this opportunity
    like never before. But first, we must be honest about the challenges we face. While they are plentiful, they
    will be annihilated by this great momentum that the world is now witnessing in the United States of America.
    As we gather today, our government confronts a crisis of trust. For many years, a radical and corrupt
    establishment has extracted power and wealth from our citizens while the pillars of our society lay broken and
    seemingly in complete disrepair. We now have a government that cannot manage even a simple crisis at home
    while, at the same time, stumbling into a continuing catalogue of catastrophic events abroad. It fails to
    protect our magnificent, law-abiding American citizens but provides sanctuary and protection for dangerous
    criminals, many from prisons and mental institutions, that have illegally entered our country from all over
    the world. We have a government that has given unlimited funding to the defense of foreign borders but
    refuses to defend American borders or, more importantly, its own people. Our country can no longer deliver
    basic services in times of emergency, as recently shown by the wonderful people of North Carolina -- who have
    been treated so badly -- and other states who are still suffering from a hurricane that took place many months
    ago or, more recently, Los Angeles, where we are watching fires still tragically burn from weeks ago without
    even a token of defense. They’re raging through the houses and communities, even affecting some of the
    wealthiest and most powerful individuals in our country -- some of whom are sitting here right now. They
    don’t have a home any longer. That’s interesting. But we can’t let this happen. Everyone is unable to do
    anything about it. That’s going to change. We have a public health system that does not deliver in times of
    disaster, yet more money is spent on it than any country anywhere in the world. And we have an education
    system that teaches our children to be ashamed of themselves -- in many cases, to hate our country despite the
    love that we try so desperately to provide to them. All of this will change starting today, and it will change
    very quickly. My recent election is a mandate to completely and totally reverse a horrible betrayal, and all
    of these many betrayals that have taken place and to give the people back their faith, their wealth, their
    democracy, and, indeed, their freedom. From this moment on, America’s decline is over. Our liberties and our
    nation’s glorious destiny will no longer be denied. And we will immediately restore the integrity, competency,
    and loyalty of America’s government. Over the past eight years, I have been tested and challenged more than
    any President in our 250-year history, and I’ve learned a lot along the way. The journey to reclaim our
    republic has not been an easy one -- that, I can tell you. Those who wish to stop our cause have tried to take
    my freedom and, indeed, to take my life. Just a few months ago, in a beautiful Pennsylvania field, an
    assassin’s bullet ripped through my ear. But I felt then and believe even more so now that my life was saved
    for a reason. I was saved by God to make America great again. Thank you. Thank you. Thank you very much.
    That is why each day under our Administration of American patriots, we will be working to meet every crisis
    with dignity and power and strength. We will move with purpose and speed to bring back hope, prosperity,
    safety, and peace for citizens of every race, religion, color, and creed. For American citizens, January
    20th, 2025, is Liberation Day. It is my hope that our recent presidential election will be remembered as the
    greatest and most consequential election in the history of our country. As our victory showed, the entire
    nation is rapidly unifying behind our agenda with dramatic increases in support from virtually every element
    of our society: young and old, men and women, African Americans, Hispanic Americans, Asian Americans, urban,
    suburban, rural. And very importantly, we had a powerful win in all seven swing states; and the popular vote,
    we won by millions of people. To the Black and Hispanic communities, I want to thank you for the tremendous
    outpouring of love and trust that you have shown me with your vote. We set records, and I will not forget it.
    I’ve heard your voices in the campaign, and I look forward to working with you in the years to come. Today is
    Martin Luther King Day. And his honor -- this will be a great honor. But in his honor, we will strive together
    to make his dream a reality. We will make his dream come true. Thank you. Thank you. Thank you. National
    unity is now returning to America, and confidence and pride is soaring like never before. In everything we do,
    my Administration will be inspired by a strong pursuit of excellence and unrelenting success. We will not
    forget our country, we will not forget our Constitution, and we will not forget our God. Can’t do that.
    Today, I will sign a series of historic executive orders. With these actions, we will begin the complete
    restoration of America and the revolution of common sense. It’s all about common sense. First, I will declare
    a national emergency at our southern border. All illegal entry will immediately be halted, and we will begin
    the process of returning millions and millions of criminal aliens back to the places from which they came. We
    will reinstate my Remain in Mexico policy. I will end the practice of catch and release. And I will send
    troops to the southern border to repel the disastrous invasion of our country. Under the orders I sign today,
    we will also be designating the cartels as foreign terrorist organizations. And by invoking the Alien Enemies
    Act of 1798, I will direct our government to use the full and immense power of federal and state law
    enforcement to eliminate the presence of all foreign gangs and criminal networks bringing devastating crime to
    U.S. soil, including our cities and inner cities. As Commander-in-Chief, I have no higher responsibility than
    to defend our country from threats and invasions, and that is exactly what I am going to do. We will do it at
    a level that nobody has ever seen before. Next, I will direct all members of my cabinet to marshal the vast
    powers at their disposal to defeat what was record inflation and rapidly bring down costs and prices. The
    inflation crisis was caused by massive overspending and escalating energy prices, and that is why today I will
    also declare a national energy emergency. We will drill, baby, drill. America will be a manufacturing nation
    once again, and we have something that no other manufacturing nation will ever have -- the largest amount of
    oil and gas of any country on earth -- and we are going to use it. We’ll use it. We will bring prices down,
    fill our strategic reserves up again right to the top, and export American energy all over the world. We will
    be a rich nation again, and it is that liquid gold under our feet that will help to do it. With my actions
    today, we will end the Green New Deal, and we will revoke the electric vehicle mandate, saving our auto
    industry and keeping my sacred pledge to our great American autoworkers. In other words, you’ll be able to buy
    the car of your choice. We will build automobiles in America again at a rate that nobody could have dreamt
    possible just a few years ago. And thank you to the autoworkers of our nation for your inspiring vote of
    confidence. We did tremendously with their vote. I will immediately begin the overhaul of our trade system to
    protect American workers and families. Instead of taxing our citizens to enrich other countries, we will
    tariff and tax foreign countries to enrich our citizens. For this purpose, we are establishing the External
    Revenue Service to collect all tariffs, duties, and revenues. It will be massive amounts of money pouring into
    our Treasury, coming from foreign sources. The American dream will soon be back and thriving like never
    before. To restore competence and effectiveness to our federal government, my Administration will establish
    the brand-new Department of Government Efficiency. After years and years of illegal and unconstitutional
    federal efforts to restrict free expression, I also will sign an executive order to immediately stop all
    government censorship and bring back free speech to America. Never again will the immense power of the state
    be weaponized to persecute political opponents -- something I know something about. We will not allow that to
    happen. It will not happen again. Under my leadership, we will restore fair, equal, and impartial justice
    under the constitutional rule of law. And we are going to bring law and order back to our cities. This week,
    I will also end the government policy of trying to socially engineer race and gender into every aspect of
    public and private life. We will forge a society that is colorblind and merit-based. As of today, it will
    henceforth be the official policy of the United States government that there are only two genders: male and
    female. This week, I will reinstate any service members who were unjustly expelled from our military for
    objecting to the COVID vaccine mandate with full back pay. And I will sign an order to stop our warriors from
    being subjected to radical political theories and social experiments while on duty. It’s going to end
    immediately. Our armed forces will be freed to focus on their sole mission: defeating America’s enemies.
    Like in 2017, we will again build the strongest military the world has ever seen. We will measure our success
    not only by the battles we win but also by the wars that we end -- and perhaps most importantly, the wars we
    never get into. My proudest legacy will be that of a peacemaker and unifier. That’s what I want to be: a
    peacemaker and a unifier. I’m pleased to say that as of yesterday, one day before I assumed office, the
    hostages in the Middle East are coming back home to their families. Thank you. America will reclaim its
    rightful place as the greatest, most powerful, most respected nation on earth, inspiring the awe and
    admiration of the entire world. A short time from now, we are going to be changing the name of the "Gulf of
    Mexico" to the "Gulf of America" and we will restore the name of a great President, William McKinley, to
    "Mount McKinley," where it should be and where it belongs. President McKinley made our country very rich
    through tariffs and through talent -- he was a natural businessman -- and gave Teddy Roosevelt the money for
    many of the great things he did, including the Panama Canal, which has foolishly been given to the country of
    Panama after the United Spates -- the United States -- I mean, think of this -- spent more money than ever
    spent on a project before and lost 38,000 lives in the building of the Panama Canal. We have been treated
    very badly from this foolish gift that should have never been made, and Panama’s promise to us has been
    broken. The purpose of our deal and the spirit of our treaty has been totally violated. American ships are
    being severely overcharged and not treated fairly in any way, shape, or form. And that includes the United
    States Navy. And above all, China is operating the Panama Canal. And we didn’t give it to China. We gave it to
    Panama, and we’re taking it back. Above all, my message to Americans today is that it is time for us to once
    again act with courage, vigor, and the vitality of history’s greatest civilization. So, as we liberate our
    nation, we will lead it to new heights of victory and success. We will not be deterred. Together, we will end
    the chronic disease epidemic and keep our children safe, healthy, and disease-free. The United States will
    once again consider itself a growing nation -- one that increases our wealth, expands our territory, builds
    our cities, raises our expectations, and carries our flag into new and beautiful horizons. And we will pursue
    our manifest destiny into the stars, launching American astronauts to plant the Stars and Stripes on the
    planet Mars. Ambition is the lifeblood of a great nation, and, right now, our nation is more ambitious than
    any other. There’s no nation like our nation. Americans are explorers, builders, innovators, entrepreneurs,
    and pioneers. The spirit of the frontier is written into our hearts. The call of the next great adventure
    resounds from within our souls. Our American ancestors turned a small group of colonies on the edge of a vast
    continent into a mighty republic of the most extraordinary citizens on Earth. No one comes close. Americans
    pushed thousands of miles through a rugged land of untamed wilderness. They crossed deserts, scaled mountains,
    braved untold dangers, won the Wild West, ended slavery, rescued millions from tyranny, lifted billions from
    poverty, harnessed electricity, split the atom, launched mankind into the heavens, and put the universe of
    human knowledge into the palm of the human hand. If we work together, there is nothing we cannot do and no
    dream we cannot achieve. Many people thought it was impossible for me to stage such a historic political
    comeback. But as you see today, here I am. The American people have spoken. I stand before you now as proof
    that you should never believe that something is impossible to do. In America, the impossible is what we do
    best. From New York to Los Angeles, from Philadelphia to Phoenix, from Chicago to Miami, from Houston to
    right here in Washington, D.C., our country was forged and built by the generations of patriots who gave
    everything hey had for our rights and for our freedom. They were farmers and soldiers, cowboys and factory
    workers, steelworkers and coal miners, police officers and pioneers who pushed onward, marched forward, and
    let no obstacle defeat their spirit or their pride. Together, they laid down the railroads, raised up the
    skyscrapers, built great highways, won two world wars, defeated fascism and communism, and triumphed over
    every single challenge that they faced. After all we have been through together, we stand on the verge of the
    four greatest years in American history. With your help, we will restore America promise and we will rebuild
    the nation that we love -- and we love it so much. We are one people, one family, and one glorious nation
    under God. So, to every parent who dreams for their child and every child who dreams for their future, I am
    with you, I will fight for you, and I will win for you. We’re going to win like never before. Thank you.
    Thank you. Thank you. Thank you. In recent years, our nation has suffered greatly. But we are going to bring
    it back and make it great again, greater than ever before. We will be a nation like no other, full of
    compassion, courage, and exceptionalism. Our power will stop all wars and bring a new spirit of unity to a
    world that has been angry, violent, and totally unpredictable. America will be respected again and admired
    again, including by people of religion, faith, and goodwill. We will be prosperous, we will be proud, we will
    be strong, and we will win like never before. We will not be conquered, we will not be intimidated, we will
    not be broken, and we will not fail. From this day on, the United States of America will be a free, sovereign,
    and independent nation. We will stand bravely, we will live proudly, we will dream boldly, and nothing will
    stand in our way because we are Americans. The future is ours, and our golden age has just begun. The golden
    age of America begins right now. From this day forward, our country will flourish and be respected again all
    over the world. We will be the envy of every nation, and we will not allow ourselves to be taken advantage of
    any longer. During every single day of the Trump Administration, I will, very simply, put America first. Our
    sovereignty will be reclaimed. Our safety will be restored. The scales of justice will be rebalanced. The
    vicious, violent, and unfair weaponization of the Justice Department and our government will end. And our top
    priority will be to create a nation that is proud, prosperous, and free. America will soon be greater,
    stronger, and far more exceptional than ever before. I return to the presidency confident and optimistic that
    we are at the start of a thrilling new era of national success. A tide of change is sweeping the country,
    sunlight is pouring over the entire world, and America has the chance to seize this opportunity like never
    before. But first, we must be honest about the challenges we face. While they are plentiful, they will be
    annihilated by this great momentum that the world is now witnessing in the United States of America. As we
    gather today, our government confronts a crisis of trust. For many years, a radical and corrupt establishment
    has extracted power and wealth from our citizens while the pillars of our society lay broken and seemingly in
    complete disrepair. We now have a government that cannot manage even a simple crisis at home while, at the
    same time, stumbling into a continuing catalogue of catastrophic events abroad. It fails to protect our
    magnificent, law-abiding American citizens but provides sanctuary and protection for dangerous criminals, many
    from prisons and mental institutions, that have illegally entered our country from all over the world. We
    have a government that has given unlimited funding to the defense of foreign borders but refuses to defend
    American borders or, more importantly, its own people. Our country can no longer deliver basic services in
    times of emergency, as recently shown by the wonderful people of North Carolina -- who have been treated so
    badly -- and other states who are still suffering from a hurricane that took place many months ago or, more
    recently, Los Angeles, where we are watching fires still tragically burn from weeks ago without even a token
    of defe nse. They’re raging through the houses and communities, even affecting some of the wealthiest and most
    powerful individuals in our country -- some of whom are sitting here right now. They don’t have a home any
    longer. That’s interesting. But we can’t let this happen. Everyone is unable to do anything about it. That’s
    going to change. We have a public health system that does not deliver in times of disaster, yet more money is
    spent on it than any country anywhere in the world. And we have an education system that teaches our children
    to be ashamed of themselves -- in many cases, to hate our country despite the love that we try so desperately
    to provide to them. All of this will change starting today, and it will change very quickly. My recent
    election is a mandate to completely and totally reverse a horrible betrayal, and all of these many betrayals
    that have taken place and to give the people back their faith, their wealth, their democracy, and, indeed,
    their freedom. From this moment on, America’s decline is over. Our liberties and our nation’s glorious destiny
    will no longer be denied. And we will immediate ly restore the integrity, competency, and loyalty of America’s
    government. Over the past eight years, I have been tested and challenged more than any President in our
    250-year history, and I’ve learned a lot along the way. The journey to reclaim our republic has not been an
    easy one -- that, I can tell you. Those who wish to stop our cause have tried to take my freedom and, indeed,
    to take my life. Just a few months ago, in a beautiful Pennsylvania field, an assassin’s bullet ripped through
    my ear. But I felt then and believe even more so now that my life was saved for a reason. I was saved by God
    to make America great again. Thank you. Thank you. Thank you very much. That is why each day under our
    Administration of American patriots, we will be working to meet every crisis with dignity and power and
    strength. We will move with purpose and speed to bring back hope, prosperity, safety, and peace for citizens
    of every race, religion, color, and creed. For American citizens, January 20th, 2025, is Liberation Day. It
    is my hope that our recent presidential election will be remembered as the greatest and most consequential
    election in the history of our country. As our victory showed, the entire nation is rapidly unifying behind
    our agenda with dramatic increases in support from virtually every element of our society: young and old, men
    and women, African Americans, Hispanic Americans, Asian Americans, urban, suburban, rural. And very
    importantly, we had a powerful win in all seven swing states; and the popular vote, we won by millions of
    people. To the Black and Hispanic communities, I want to thank you for the tremendous outpouring of love and
    trust that you have shown me with your vote. We set records, and I will not forget it. I’ve heard your voices
    in the campaign, and I look forward to working with you in the years to come. Today is Martin Luther King
    Day. And his honor -- this will be a great honor. But in his honor, we will strive together to make his dream
    a reality. We will make his dream come true. Thank you. Thank you. Thank you. National unity is now
    returning to America, and confidence and pride is soaring like never before. In everything we do, my
    Administration will be inspired by a strong pursuit of excellence and unrelenting success. We will not forget
    our country, we will not forget our Constitution, and we will not forget our God. Can’t do that. Today, I
    will sign a series of historic executive orders. With these actions, we will begin the complete restoration of
    America and the revolution of common sense. It’s all about common sense. First, I will declare a national
    emergency at our southern border. All illegal entry will immediately be halted, and we will begin the process
    of returning millions and millions of criminal aliens back to the places from which they came. We will
    reinstate my Remain in Mexico policy. I will end the practice of catch and release. And I will send troops to
    the southern border to repel the disastrous invasion of our country. Under the orders I sign today, we will
    also be designating the cartels as foreign terrorist organizations. And by invoking the Alien Enemies Act of
    1798, I will direct our government to use the full and immense power of federal and state law enforcement to
    eliminate the presence of all foreign gangs and criminal networks bringing devastating crime to U.S. soil,
    including our cities and inner cities. As Commander-in-Chief, I have no higher responsibility than to defend
    our country from threats and invasions, and that is exactly what I am going to do. We will do it at a level
    that nobody has ever seen before. Next, I will direct all members of my cabinet to marshal the vast powers at
    their disposal to defeat what was record inflation and rapidly bring down costs and prices. The inflation
    crisis was caused by massive overspending and escalating energy prices, and that is why today I will also
    declare a national energy emergency. We will drill, baby, drill. America will be a manufacturing nation once
    again, and we have something that no other manufacturing nation will ever have -- the largest amount of oil
    and gas of any country on earth -- and we are going to use it. We’ll use it. We will bring prices down, fill
    our strategic reserves up again right to the top, and export American energy all over the world. We will be a
    rich nation again, and it is that liquid gold under our feet that will help to do it. With my actions today,
    we will end the Green New Deal, and we will revoke the electric vehicle mandate, saving our auto industry and
    keeping my sacred pledge to our great American autoworkers. In other words, you’ll be able to buy the car of
    your choice. We will build automobiles in America again at a rate that nobody could have dreamt possible just
    a few years ago. And thank you t o the autoworkers of our nation for your inspiring vote of confidence. We did
    tremendously with their vote. I will immediately begin the overhaul of our trade system to protect American
    workers and families. Instead of taxing our citizens to enrich other countries, we will tariff and tax foreign
    countries to enrich our citizens. For this purpose, we are establishing the External Revenue Service to
    collect all tariffs, duties, and revenues. It will be massive amounts of money pouring into our Treasury,
    coming from foreign sources. The American dream will soon be back and thriving like never before. To restore
    competence and effectiveness to our federal government, my Administration will establish the brand-new
    Department of Government Efficiency. After years and years of illegal and unconstitutional federal efforts to
    restrict free expression, I also will sign an executive order to immediately stop all government censorship
    and bring back free speech to America. Never again will the immense power of the state be weaponized to
    persecute political opponents -- something I know something about. We will not allow that to happen . It will
    not happen again. Under my leadership, we will restore fair, equal, and impartial justice under the
    constitutional rule of law. And we are going to bring law and order back to our cities. This week, I will
    also end the government policy of trying to socially engineer race and gender into every aspect of public and
    private life. We will forge a society that is colorblind and merit-based. As of today, it will henceforth be
    the official policy of the United States government that there are only two genders: male and female. This
    week, I will reinstate any service members who were unjustly expelled from our military for objecting to the
    COVID vaccine mandate with full back pay. And I will sign an order to stop our warriors from being subjected
    to radical political theories and social experiments while on duty. It’s going to end immediately. Our armed
    forces will be freed to focus on their sole mission: defeating America’s enemies. Like in 2017, we will again
    build the strongest military the world has ever seen. We will measure our success not only by the battles we
    win but also by the wars that we end -- and perhaps most importantly, the wars we never get into. My proudest
    legacy will be that of a peacemaker and unifier. That’s what I want to be: a peacemaker and a unifier. I’m
    pleased to say that as of yesterday, one day before I assumed office, the hostages in the Middle East are
    coming back home to their families. Thank you. America will reclaim its rightful place as the greatest, most
    powerful, most respected nation on earth, inspiring the awe and admiration of the entire world. A short time
    from now, we are going to be changing the name of the "Gulf of Mexico" to the "Gulf of America" and we will
    restore the name of a great President, William McKinley, to "Mount McKinley," where it should be and where it
    belongs. President McKinley made our country very rich through tariffs and through talent -- he was a natural
    businessman -- and gave Teddy Roosevelt the money for many of the great things he did, including the Panama
    Canal, which has foolishly been given to the country of Panama after the United Spates -- the United States --
    I mean, think of this -- spent more money than ever spent on a p roject before and lost 38,000 lives in the
    building of the Panama Canal. We have been treated very badly from this foolish gift that should have never
    been made, and Panama’s promise to us has been broken. The purpose of our deal and the spirit of our treaty
    has been totally violated. American ships are being severely overcharged and not treated fairly in any way,
    shape, or form. And that includes the United States Navy. And above all, China is operatin g the Panama Canal.
    And we didn’t give it to China. We gave it to Panama, and we’re taking it back. Above all, my message to
    Americans today is that it is time for us to once again act with courage, vigor, and the vitality of history’s
    greatest civilization. So, as we liberate our nation, we will lead it to new heights of victory and success.
    We will not be deterred. Together, we will end the chronic disease epidemic and keep our children safe,
    healthy, and disease-free. The United States will once again consider itself a growing nation -- one that
    increases our wealth, expands our territory, builds our cities, raises our expectations, and carries our flag
    into new and beautiful horizons. And we will pursue our manifest destiny into the stars, launching American
    astronauts to plant the Stars and Stripes on the planet Mars. Ambition is the lifeblood of a great nation,
    and, right now, our nation is more ambitious than any other. There’s no nation like our nation. Americans are
    explorers, builders, innovators, entrepreneurs, and pioneers. The spirit of the frontier is written into our
    hearts. The call of the next great adventure resounds from within our souls. Our American ancestors turned a
    small group of colonies on the edge of a vast continent into a mighty republic of the most extraordinary
    citizens on Earth. No one comes close. Americans pushed thousands of miles through a rugged land of untamed
    wilderness. They crossed deserts, scaled mountains, braved untold dangers, won the Wild West, ended slavery,
    rescued millions from tyranny, lifted billions from poverty, harnessed electricity, split the atom, launched
    mankind into the heavens, and put the universe of human knowledge into the palm of the human hand . If we work
    together, there is nothing we cannot do and no dream we cannot achieve. Many people thought it was impossible
    for me to stage such a historic political comeback. But as you see today, here I am. The American people have
    spoken. I stand before you now as proof that you should never believe that something is impossible to do. In
    America, the impossible is what we do best. From New York to Los Angeles, from Philadelphia to Phoenix, from
    Chicago to Miami, from Houston to right here in Washington, D.C., our country was forged and built by the
    generations of patriots who gave everything hey had for our rights and for our freedom. They were farmers and
    soldiers, cowboys and factory workers, steelworkers and coal miners, police officers and pioneers who p ushed
    onward, marched forward, and let no obstacle defeat their spirit or their pride. Together, they laid down the
    railroads, raised up the skyscrapers, built great highways, won two world wars, defeated fascism and
    communism, and triumphed over every single challenge that they faced. After all we have been through
    together, we stand on the verge of the four greatest years in American history. With your help, we will
    restore America promise and we will rebuild the nation that we love -- and we love it so much. We are one
    people, one family, and one glorious nation under God. So, to every parent who dreams for their child and
    every child who dreams for their futu re, I am with you, I will fight for you, and I will win for you. We’re
    going to win like never before. Thank you. Thank you. Thank you. Thank you. In recent years, our nation has
    suffered greatly. But we are going to bring it back and make it great again, greater than ever before. We
    will be a nation like no other, full of compassion, courage, and exceptionalism. Our power will stop all wars
    and bring a new spirit of unity to a world that has been angry, violent, and totally unpredictable. America
    will be respected again and admired again, including by people of religion, faith, and goodwill. We will be
    prosperous, we will be proud, we will be strong, and we will win like never before. We will not be conquered,
    we will not be intimidated, we will not be broken, and we will not fail. From this day on, the United States
    of America will be a free, sovereign, and independent nation. We will stand bravely, we will live proudly, we
    will dream boldly, and nothing will stand in our way because we are Americans. The future is ours, and our
    golden age has just begun.
    ;;;;
    run;quit;

    858-551

    */ /**************************************************************************************************************************/
    */ /* SD1.BPASSAGE total obs=1
    */ /* Obs
    */ /*
    */ /*  1  The golden age of America begins right now From this day
    */ /*
    */ /*  -- CHARACTER --
    */ /* Variable          Typ      Value
    */ /*
    */ /* PASSAGE            C32756  The golden age of America b...
    */ /* TOTOBS             C16   1
    */ /*
    */ /**************************************************************************************************************************/

    proc format;
     value $tok2grammer
      "CC  "="Coordinating conjunction                "
      "CD  "="Cardinal number                         "
      "DT  "="Determiner                              "
      "EX  "="Existential there                       "
      "FW  "="Foreign word                            "
      "IN  "="Preposition or subordinating conjunction"
      "JJ  "="Adjective                               "
      "JJR "="Adjective, comparative                  "
      "JJS "="Adjective, superlative                  "
      "LS  "="List item marker                        "
      "MD  "="Modal                                   "
      "NN  "="Noun, singular or mass                  "
      "NNS "="Noun, plural                            "
      "NNP "="Proper noun, singular                   "
      "NNPS"="Proper noun, plural                     "
      "PDT "="Predeterminer                           "
      "POS "="Possessive ending                       "
      "PRP "="Personal pronoun                        "
      "PRP$"="Possessive pronoun                      "
      "RB  "="Adverb                                  "
      "RBR "="Adverb, comparative                     "
      "RBS "="Adverb, superlative                     "
      "RP  "="Particle                                "
      "SYM "="Symbol                                  "
      "UH  "="Interjection                            "
      "VB  "="Verb, base form                         "
      "VBD "="Verb, past tense                        "
      "VBG "="Verb, gerund or present participle      "
      "VBN "="Verb, past participle                   "
      "VBP "="Verb, non­3rd person singular present   "
      "VBZ "="Verb, 3rd person singular present       "
      "WDT "="Wh­determiner                           "
      "WP  "="Wh­pronoun                              "
      "WP$ "="Possessive wh­pronoun                   "
      "WRB "="Wh­adverb                               "
      other="Preposition"
    ;run;quit;

    /*
     _ __  _ __ ___   ___ ___  ___ ___
    | `_ \| `__/ _ \ / __/ _ \/ __/ __|
    | |_) | | | (_) | (_|  __/\__ \__ \
    | .__/|_|  \___/ \___\___||___/___/
    |_|
    */

    proc datasets lib=sd1 nolist nodetails;
     delete bwant;
    run;quit;

    %utl_rbeginx;
    parmcards4;
    library(stringr)
    library(NLP)
    library(openNLP)
    library(haven)
    source("c:/oto/fn_tosas9x.R")
    txt<-read_sas("d:/sd1/bpassage.sas7bdat")
    txt
    s <- as.String(txt$PASSAGE)
    sent_token_annotator<-
      Maxent_Sent_Token_Annotator()
    word_token_annotator <-
      Maxent_Word_Token_Annotator()
    a2 <- annotate(s
     ,list(sent_token_annotator
     ,word_token_annotator))
    pos_tag_annotator <-
      Maxent_POS_Tag_Annotator()
    pos_tag_annotator
    a3 <- annotate(s
      ,pos_tag_annotator
      ,a2)
    head(annotate(s
     ,Maxent_POS_Tag_Annotator(probs=TRUE)
     ,a2))
    a3w <- subset(a3, type == "word")
    tags <- sapply(a3w$features,`[[`,"POS")
    table(tags)
    want<-as.data.frame(sprintf("%s/%s"
     ,s[a3w], tags))
    colnames(want)<-"wrdGrm"
    fn_tosas9x(
          inp    = want
         ,outlib ="d:/sd1/"
         ,outdsn ="bwant"
         )
    ;;;;
    %utl_rendx;

    /**************************************************************************************************************************/
    /* SD1.BWANT total obs5 5,675                                                                                             */
    /*                                                                                                                        */
    /*  Obs    ROWNAMES    WRDGRM                                                                                             */
    /*                                                                                                                        */
    /*    1        1       The/DT                                                                                             */
    /*    2        2       golden/JJ                                                                                          */
    /*    3        3       age/NN                                                                                             */
    /*    4        4       of/IN                                                                                              */
    /*    5        5       America/NNP                                                                                        */
    /*                                                                                                                        */
    /* 5672      5672      age/NN                                                                                             */
    /* 5673      5673      has/VBZ                                                                                            */
    /* 5674      5674      just/RB                                                                                            */
    /* 5675      5675      begun/VBN                                                                                          */
    /*************************************************************************************************************************

    data btemp ;
      set sd1.bwant;
      word=scan(wrdGrm,1,'/');
      grm=scan(wrdGrm,2,'/');
      grammer=put(strip(grm)
      ,$tok2grammer.);
      if grammer=:"Verb, past participle";
      if word ="been" then delete;
       keep word grammer;
    run;quit;

    /**************************************************************************************************************************/
    /* ATEMP total obs=119 Subset of verbs                                                                                    */
    /*                                                                                                                        */
    /* Obs    WORD                  GRAMMER                                                                                   */
    /*                                                                                                                        */
    /*   1    respected      Verb, past participle                                                                            */
    /*   2    taken          Verb, past participle                                                                            */
    /*   3    reclaimed      Verb, past participle                                                                            */
    /*   4    restored       Verb, past participle                                                                            */
    /*   5    rebalanced     Verb, past participle                                                                            */
    /*   6    annihilated    Verb, past participle                                                                            */
    /* ...                                                                                                                    */
    /* 115    respected      Verb, past participle                                                                            */
    /* 116    conquered      Verb, past participle                                                                            */
    /* 117    intimidated    Verb, past participle                                                                            */
    /* 118    broken         Verb, past participle                                                                            */
    /* 119    begun          Verb, past participle                                                                            */
    /**************************************************************************************************************************/

    proc freq data=btemp order=freq;
     tables word / list out=sd1.pres2
        (keep=word count rename=word=cat);
    run;quit;

    /**************************************************************************************************************************/
    /* Obs    CAT            COUNT                                                                                            */
    /*                                                                                                                        */
    /*   1    broken           6                                                                                              */
    /*   2    spent            6                                                                                              */
    /*   3    treated          6                                                                                              */
    /*   4    built            4                                                                                              */
    /*   5    given            4                                                                                              */
    /* ....                                                                                                                   */
    /*  43    tried            2                                                                                              */
    /*  44    violated         2                                                                                              */
    /*  45    weaponized       2                                                                                              */
    /*  46    written          2                                                                                              */
    /*  47    ushed            1                                                                                              */
    /**************************************************************************************************************************/

    /*              _
      ___ _ __   __| |
     / _ \ `_ \ / _` |
    |  __/ | | | (_| |
     \___|_| |_|\__,_|

    */
