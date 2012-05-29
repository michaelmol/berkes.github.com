---
layout: post_archive
title: Hoe veilig is openID nu eigenlijk?
created: 1197051488
tags:
- Server
- Open Source
- internet
- openID
- Identity
lang: nl
---
openId wekt veel verwarring bij veel mensen. Laat ik daarom kort en bondig proberen uit te leggen hoe het eigenlijk werkt: wat de idee achter openID is.**openID Doelstelling:** Je privé gegevens maar op één veilige, centrale plek opslaan.**Servers:** OpenID is open. Het staat iedereen, dus ook jou, en dus ook de maffia of onze overheid, vrij om een openID server te beginnen. De server is de plek waar jij je eenmalig registreert en waar jij je gegevens opslaat. Stel dat we een vooruitstrevende overheid hadden gehad, dan zou die een openID provider kunnen worden, een openID server gaan beheren dus. Op bijvoorbeeld: uwgegevens.nl. uwgegevens.nl is heel goed beveiligd, je kunt alleen inloggen met je paspoortnummer, een vingerafdruk enzovoort. Stel jij vertrouwt de overheid genoeg, om daar je gegevens, zoals je mailadres je naam, je foto en eventueel je postadres achter te laten. Dan maak jij een profiel aan op uwgegevens.nl, en is je openid **berkes.uwgegevens.nl**.

Het is dus van cruciaal dat jij een betrouwbare openIDprovider kiest. Ten eerste kunnen zij bij alle gegevens die je achterlaat. Ten tweede ben je écht de pineut als iemand weet in te breken op je openID provider.

Daarom is bijvoorbeeld een bank een goede openID provider. profiel.rabobank.nl bijvoorbeeld, waar je inlogt met je random-reader, zou zeer betrouwbaar zijn!**OpenID Clients:** Iedere andere site kan nu openID-inlog diensten bieden. Bijvoorbeeld [blogger.com](http://blogger.com) is sinds kort een openID client. Als ik op blogger.com een reactie wil achterlaten, kan dat met mijn openID berkes.uwgegevens.nl. Blogger stuurt mij dan door naar berkes.uwgegevens.nl, waar ik moet inloggen. **Ik hoef dus geen wachtwoorden, random-readers mailadressen of wat dan ook op blogger.com in te voeren**. Het enige dat blogger.com weet, is dat mijn openID  berkes.uwgegevens.nl is. ze weten dus niet waar ik woon, wat mijn mailadres is, of wat mijn bankrekeningnummer is. Als ik ingelogd ben op berkes.uwgegevens.nl, kan ik aldaar opgeven, **of** ik uberhaupt wil inloggen op blogger.com, **wat** blogger.com van me mag weten en **hoelang** blogger.com deze openID mag gebruiken. Blogger.com stuurt ook nog een vraag mee, waarin verteld wordt aan uwgegevens.nl welke gegevens blogger.com graag wil hebben. Mailadres, banknummer en postcode bijvoorbeeld. berkes.uwgegevens.nl toont dat aan mij als ik voor het eerst mijn openID wil gebruiken. Zodoende kan ik op berkes.uwgegevens.nl aangeven dat ik niet accoord ga met het doorgeven van mijn banknummer bijvoorbeeld. Nadat ik blogger.com goedgekeurd heb op berkes.uwgegevens.nl, wordt ik weer teruggestuurd naar blogger.com, waar ik vanaf nu reacties kan achterlaten. En krijgt blogger.com een seintje dat ik me op correct berkes.uwgegevens.nl heb ingelogd. En krijgt blogger.com de door mij goedgekeurde gegevens meegestuurd. blogger.com krijgt dus nooit mijn wachtwoorden, of andere informatie die ik niet wil vrijgeven door!**voordelen** ten opzichte van registreren op blogger.com zijn, dat _ik_ precies kan bepalen wat blogger.com van me mag weten. Ook hoef ik niet overal een wachtwoord in te voeren. Ik ken genoeg mensen die overal hetzelfde wachtwoord gebruiken. Omdat ik een heleboel sites beheer, weet ik dus bijna zeker van een heleboel mensen wat hun wachtwoord van hun thuiscomputer, hotmail, postbank enzovoort is. Dat probleem is niet langer aan de orde met openID.

Verder heb je nog maar één plek waar je je gegevens bijhoud, kun je dus ten alle tijden ook op één plek je details aanpassen, of weggooien. **nadelen** ten opzichte van registreren op jan-en-alleman's sites, is dat ik de openID provider heel goed moet vertrouwen. Want als daar wordt ingebroken, of als zij je gegevens vrolijk verkopen, dan ben je goed de sjaak, want dan kunnen ze vervolgens onder jou naam bijvoorbeeld reacties op blogger.com achterlaten.

Ook kan een site je naar een nep-openID provider doorsturen. Stel dan gratis-viagra.to een openID inlog heeft, en jou, in plaats van naar berkes.uwgegevens.nl (wat je invoerde, dus) stuurt, maar naar berkes.uwgegeven**z**.nl (met een z) waar ze precies de officiele site nabouwden. Dan geef jij daar je inloggegevens in die je normaal op berkes.uwgegevens.nl invoerde. En kunnen zij dus bij al je inlogsites komen, inclusief al je privegegevens. Dit laatste heet phishing trouwens. Je zult dus steeds extra goed moeten opletten.