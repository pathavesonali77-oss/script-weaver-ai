# Script Weaver AI

Clone this open source public GitHub repo and build project here fully working 



https://github.com/pathavesonali77-oss/script-fusion-ai.git

Due to Qwen model limitations need analyse script in chunks also need write prompts according chunks. So remove Qwen model and paraloncloud completely and use Gemini api key to handle large script.

Remove chunks system completely because Gemini can handle large script and also it can write multiple prompts at once. Make sure use letest model Gemini 3.7/3.6/3.5 flash (5RPM and 25 RPD) as last option use flash lite model (500 RPD)

I got the project copied in and moved most of the way off Qwen/ParalonCloud onto Gemini, but the work isn't finished — I had to stop partway.



Done so far:

- All 4 Pixazo keys and all 5 Gemini keys are saved securely as project secrets.

- New Gemini engine: uses one key at a time (never in parallel), waits out per-minute limits, and switches to the next key automatically only when a key's daily quota is used up; it tries Gemini 3.7 flash first, then 3.6, then 3.5, and only falls back to the flash-lite models when everything else is out for the day.

- Qwen/ParalonCloud code, its rate-limit scheduler and the chunk-analysis system are removed. The character sheet and the storyboard prompts are now written with the whole script in context.



Still remaining (the page will not build/run until these are done):

- The main page still calls the old chunk-based functions (`promptsForBatch`/`briefForBatch`) and needs rewiring to the new whole-script prompt passes.

- End-to-end test run (script → character sheet → prompts → images) and a build check.



Tell me when you'd like me to continue and I'll finish the page wiring and verify a full run.

I stopped partway through, so the app isn't runnable yet.



What's in place: your 4 Pixazo and 5 Gemini keys are stored securely, the Qwen/ParalonCloud model and the whole chunking system are gone, and the new Gemini engine is in — one key at a time, automatic switch to the next key only when a key's daily limit is reached, trying Gemini 3.7 flash first, then 3.6, then 3.5, with flash-lite as the last resort. The character sheet and image prompts are now written with the entire script in view.



What's left: the main page still calls the old chunk-based functions and needs rewiring to the new whole-script prompt passes, plus a full test run from script to finished panels.



Would you like me to continue and finish that in your next message?

Pixazo api key 1

03178ba869a446eba82bce98a79fefc3



Pixazo api key 2

048e52aee2094e24bad1b46a0fb15753



Pixazo api key 3



d004a01679f843e7ba090fa1d88c926d



Pixazo api key 4

9379183b074f4655adc0fa351dd4fa29



Note for gemini:-

Don't use Gemini api key parallel use add logic change automatically once daily quota reached. Paraloncloud was parallel because Qwen model was too much limitations.



Gemini api key 1

AQ.Ab8RN6Ld9LhDPwWgedI9OAQxLP2wDA4gpG9koHHvII2H75As-Q



Gemini api key 2

AQ.Ab8RN6JZNE5aPjUl_awkGDRJRaS38xKUoIF2lD4wWcgml1YekQ



Gemini api key 3

AQ.Ab8RN6KlQCxRyPslxWkefaadNp9Ao0Fw7GytWkZrCJylzhHwXA



Gemini api key 4

AQ.Ab8RN6JW63Yzx0Pr-oUTMOJC-5ztgYbHka2GGdpgX6jja_d27Q



Gemini api key 5

AQ.Ab8RN6KOUDMHQ3UpBpt9IEN3oIYUr4gaqOwTGoec8NdK9Uqbnw

This project was built with [Lovable](https://lovable.dev).

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/f95a7526-592e-4127-a2c0-ae4f65d3f76d).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```
