---
title: Some musing on ChRIS and Cloud Technologies 
authors: rudolph 
tags: [musings, historical, OpenShift, future]
---

I have found myself of late trying to explain a bit how ChRIS relates to the "Cloud". How does ChRIS benefit from cloud technologies and build compelling solutions? Usually in the mix is the term "AI". I suppose each of these concepts, "ChRIS", "Cloud", "AI" are fully deserving of their own blogs. Still, in the interest of just tackling a question that I have been asked about, and to marshal my thoughts, I'll attempt to discuss a bit about how ChRIS and also speak to how ChRIS has grown with technologies like OpenShift. I'll honor the "musings" tag line and keep this posting somewhat conversational, even though OpenShift is a specific engineering technology.

I have been working in what I'll call _scientific compute_ for more than two decades. This does of course beg the question _"What is scientific compute?"_ other than the obvious "something to do with science". From my perspective _scientific compute_ stems from a very simple design pattern: analyze data (related to some science) and produce results. That's it. No mess, no fuss. The bedrock of science of course is _data_ (or _observations_) and the purpose of science really is to map or analyze that data into something meaningful. _Scientific compute_ stays close to that ethos. In a practical sense, to me _scientific compute_ consists of input data, some analysis on that data, and output data. True, such a pattern is not exclusively _scientific_ and there are no doubt many other domains that follow something similar -- financial computing, for example. Still, as a general observation, this pattern is endemic in computing in science.

```mermaid
┌────────────┐    ┌────────────┐    ┌─────────────┐ 
│            │    │ Scientific │    │             │  
│ Input data ├───►│  Analysis  ├───►│ Output data │  
│            │    │            │    │             │ 
└────────────┘    └────────────┘    └─────────────┘ 
```

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

is reads in a bunch of data, then "crunches" it (or _computes_ on it), and saves output results. 



In thinking about this I realized I might be a bit too close to seeing "how the sausage is made". So in an effort to "get out of the factory" (and also my own head) I thought to take several steps out and back and maybe tackle this from a fresh perspective. I like to ground myself in something of a historical story, particularly if I consider future directions, so I invite you to take a seat (if so inclined) and let me ramble a bit on how ChRIS was enabled by OpenShift and how future use of that cloud technology helps us solve problems in new and innovative ways.

I keep wanting to be sidetracked about "ChRIS" itself. There is a nagging voice in my head that keeps interrupting, "You can't talk about this topic without talking about ChRIS. Or actually OpenShift for that matter." So let me just touch on that point, or part of that point, and then we can all move on. For now, let's just settle on the "What is ChRIS?". Can I, with apologies to Douglas Adams and the Sirius Cybernetics Corporation's Marketing Department, who define a robot as "Your Plastic Pal Who's Fun to Be With", come up with something as catchy? "ChRIS is your Software Pal That Makes Computing Fun". Maybe? "ChRIS is your Software Agent that Runs Your Apps... particularly your biomedical centered ones"? "ChRIS is your Shaman Who Knows the Cloud So You Don't Have To"? "ChRIS is your Software Buddy Who Is There For You and Never Asks You To Change?" Maybe not? But the voice in my head seems satisfied (it even told me, "Good ones... By the time a reader gets to the end of this, all those will make sense"). Oh dear. We'll leave OpenShift for now.

In the early 2000s, I, a newly minted PhD in biomedical engineering, started a postdoc at Massachusetts General Hospital. And, flush with the naïvety of relative youth, believed technology could unlock the secrets of medicine. And not just any technology, but specifically *computing* as wielded by the power of software. Words and logic would pry open what is hidden and it would of course be wonderful. I did mention my naïvety? I had this belief, and wasn't about to be deterred by the fact that I simply had no idea _how_, but pish-posh. Soon, I was to start a longstanding and incredibly rewarding career trajectory with Ellen Grant as mentor and collaborator. Ellen -- a clinician and clinical scientist -- and myself a wannabe computational (neuro?)scientist, very early on found common cause on this point, this belief that if pharmacology was the hallmark of 20th century medical innovation, the 21st century would rely on computing.

I think it's useful to note here that while my particular PhD research was in an AI field called "Reinforcement Learning", neither Ellen nor myself were especially fixated "AI" or "big data" or the buzz words of the 2020s. I myself had been using "neural networks" back when they weren't even considered "AI" but simply "pattern classifiers". In fact at the time of the early 2000s, AI as a field was in one of its predictable and cyclical "winters".

Speaking for myself, my belief in computing was grounded in the rich multi decade history of scientific compute. Hulking behemoths of the 1950s -- analog computers -- had been used for simulating nuclear explosions. Punch cards of the 1960s programmed the first digital computers for weather prediction. The "micro" revolution of the 1970s and 1980s brought computers into people's homes and lives. By the 1990s, medicine was using computers to better process images that peered into the very stuff of bodies. By the time I got into the field in the early 2000s computing was fundamental. Our particular field of study, neuroradiology, was a hot bed of image processing and mathematical philosophizing tied closely to imaging techniques. Diffusion tractography, an approach that _roughly_ mapped to mapping out the "wiring" of the brain was coming on line and it seemed that possibilities of combining tractography and anatomical imaging and functional MRI -- techniques that all rely ultimately on understanding mathematics and computing would push back the frontiers. The obscure branch of graph theory suddenly was in vogue as it allowed the quantification of the "connectivity" of the brain. Hubs, and small worldedness, and interconnectivity -- terms from mathematics promised to better understand how we were put together, and of course to crunch the mathematics we needed programming and computing. Again, I want to stress, no "AI" here. But certainly computing.

Of course, I doubt we were the only biomedical scientists to believe that computing was the future. I would venture most researchers in the field either implicitly or explicitly felt that. I think though, that we were soon to start experiencing our own version of reality checks that would start to powerfully shape our views. The first major reality check would come soon enough: computing might help _drive_ science, but for the most part, _scientists_ are not *programmers*. 