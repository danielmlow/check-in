![CI](https://github.com/sensein/covid19/workflows/CI/badge.svg)

# Covid19 voice protocol

This a protocol being used to help understand which activities improve wellbeing most and track changes in mental health through voice.    
 
The overall protocol is in the `protocol`folder and individual tasks and items
are in the `activity/Wellbeing` folders. 

# Technical details

1. This repo uses [ReproSchema](https://github.com/ReproNim/reproschema/),
[ReproSchema-UI](https://github.com/ReproNim/reproschema-ui/).
2. The UI is added as a submodule (`ui`) and changes relative to the UI are stored 
in `ui-changes`.
3. The entire build is carried out by Github actions and deployed via gh-pages.

Test protocol: ```https://schema.repronim.org/ui/#/?url=https://raw.githubusercontent.com/sensein/covid19/master/protocol/Covid19_schema```

Protocol:
* Landing page in `README-<language>.md` where `<language>` can be `en` or `es` for now.
* Share data
* Is today your first day of the challenge?
    * If no
        * what task did you do last time? last_activity
            * If other last_activity_other
        *  How meaningful was it? last_activity_rating
* Recorded or written journal? record_or_write        
* journaling_recorded
    * if record: multipart_audio_check
* journaling_written
* Ecological momentary assessment ema
* If Monday: would you like to answer two quick mental health surveys?
    * If yes: PHQ9 and GAD7
* List of wellbeing_items
* wellbeing_item1
* wellbeing_itemN
* Additional questionnaires more_questions



# ToDos:
* Change labels and descriptions in Wellbeing items
* check covid19 for new format

* EMA: Participants were first asked to rate how much of the following feelings and emotions they were experiencing (from “not at all” to “extremely”, 5-point scale): upset, excited, nervous, distressed, inspired, scared, alert, determined, afraid, enthusiastic. This provided a broad measure of their current positive affective state and negative affective state at the time of the ping.

* As part of wellbeing, give person feedback on their PHQ9 like Mental Health AMerica

* `{"isAbout": "PHQ9_schema", "alternateName": {"en": "Mood", "es": "Humor" }},`

* `{"variableName": "PHQ9_schema", "isVis": "(new Date().getDay()) === 1"},`

* `"preamble": {
        "en": "For each task, you should hit the record button before speaking and then stop once you are done speaking. You may hit play to hear what was recorded.",
        "es": "Para cada pregunta, debería hacer click sobre el botón antes de hablar y luego hacerlo de nuevo para parar de grabar. Luego puede tocar play para escuchar su respuesta."
    }`