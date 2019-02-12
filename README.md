# test-rel-preload
Tests to explore positioning of rel="preload" links

# Variations

| URL | Description |
|-----|-------------|
| /test-rel-preload/tests/electro/index.html | Initial templace with no changes except performance mark for fonts loaded |
| /test-rel-preload/tests/electro/index-base.html | Base page with no preload and scripts in head |
| /test-rel-preload/tests/electro/index-link-preload-start-head.html | Declarative preload at start of head |
| /test-rel-preload/tests/electro/index-link-preload-end-head.html | Declarative preload at end of head element |
| /test-rel-preload/tests/electro/index-js-inserted-link-preload.html | Script inserted preloads with snippet after blocking scripts in head |  
| /test-rel-preload/tests/electro/index-js-inserted-link-preload-v2.html |  Script inserted preloads with snippet before blocking scripts in head  |  
| /test-rel-preload/tests/electro/index-link-preload-in-body.html | Declarative preload in body element |
| /test-rel-preload/tests/electro/index-link-preload-priority-hints.html | Declarative preload with low importance priority hints |

Each of the variations is available on github, CloudFront and a test server running h2o

(there's no guarantee the h2o version will remain functioning as it's one of my playgrouds but I'll try to leave it alone for a while!)

## Github.io
https://andydavies.github.io/test-rel-preload/tests/electro/index.html  
https://andydavies.github.io/test-rel-preload/tests/electro/index-base.html  
https://andydavies.github.io/test-rel-preload/tests/electro/index-link-preload-start-head.html  
https://andydavies.github.io/test-rel-preload/tests/electro/index-link-preload-end-head.html  
https://andydavies.github.io/test-rel-preload/tests/electro/index-js-inserted-link-preload.html  
https://andydavies.github.io/test-rel-preload/tests/electro/index-js-inserted-link-preload-v2.html  
https://andydavies.github.io/test-rel-preload/tests/electro/index-link-preload-in-body.html  
https://andydavies.github.io/test-rel-preload/tests/electro/index-link-preload-priority-hints.html  


## h2o (t2.micro in AWS US East)
https://test.andydavies.me/test-rel-preload/tests/electro/index.html  
https://test.andydavies.me/test-rel-preload/tests/electro/index-base.html  
https://test.andydavies.me/test-rel-preload/tests/electro/index-link-preload-start-head.html  
https://test.andydavies.me/test-rel-preload/tests/electro/index-link-preload-end-head.html  
https://test.andydavies.me/test-rel-preload/tests/electro/index-js-inserted-link-preload.html  
https://test.andydavies.me/test-rel-preload/tests/electro/index-js-inserted-link-preload-v2.html  
https://test.andydavies.me/test-rel-preload/tests/electro/index-link-preload-in-body.html  
https://test.andydavies.me/test-rel-preload/tests/electro/index-link-preload-priority-hints.html  

## CloudFront
https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-base.html  
https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-link-preload-start-head.html  
https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-link-preload-end-head.html  
https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-js-inserted-link-preload.html  
https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-js-inserted-link-preload-v2.html  
https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-link-preload-in-body.html  
https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-link-preload-priority-hints.html  


# WebPageTest Results

Not every variation is in these results, for example CloudFront's HTTP/2 prioritisation isn't great so testing on it was abandoned quickly and Chrome's prioritisation of preloads meant there was little point tesing declarative preloads in the body.


| URL | Scenario | WPT ID | Results URL |
|-----|----------|--------|-------------|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-base.html	|	Dulles, Chrome, Cable	|	190208_RD_e7b7ae540c436d14a560baa0380f66a6	|	https://www.webpagetest.org/result/190208_RD_e7b7ae540c436d14a560baa0380f66a6/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-link-preload-start-head.html	|	Dulles, Chrome, Cable	|	190208_RK_9f482a7621373bc5328ca0feed4bbbc6	|	https://www.webpagetest.org/result/190208_RK_9f482a7621373bc5328ca0feed4bbbc6/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-js-inserted-link-preload.html	|	Dulles, Chrome, Cable	|	190211_TK_7ea3c87c174c01544b2a6c8073596b63	|	https://www.webpagetest.org/result/190211_TK_7ea3c87c174c01544b2a6c8073596b63/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-js-inserted-link-preload-v2.html	|	Dulles, Chrome, Cable	|	190211_00_bf35fa5e5965a734ca8e7d832ebd5770	|	https://www.webpagetest.org/result/190211_00_bf35fa5e5965a734ca8e7d832ebd5770/	|
|		|		|		|		|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-base.html	|	Dulles, Chrome, 3GFast	|	190208_QH_257a4da90873f7bfb2322ea67142b76e	|	https://www.webpagetest.org/result/190208_QH_257a4da90873f7bfb2322ea67142b76e/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-link-preload-start-head.html	|	Dulles, Chrome, 3GFast	|	190208_SF_f13d67a1fb2a8d126cf983f5307b7865	|	https://www.webpagetest.org/result/190208_SF_f13d67a1fb2a8d126cf983f5307b7865/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-js-inserted-link-preload.html	|	Dulles, Chrome, 3GFast	|	190211_AX_41d6fea34d431d39f29e5b1ec1067ebd	|	https://www.webpagetest.org/result/190211_AX_41d6fea34d431d39f29e5b1ec1067ebd/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-js-inserted-link-preload-v2.html	|	Dulles, Chrome, 3GFast	|	190211_CG_ba557af9207e8dc7711d5f7b5b8e0f37	|	https://www.webpagetest.org/result/190211_CG_ba557af9207e8dc7711d5f7b5b8e0f37/	|
|		|		|		|		|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-base.html	|	Dulles, Canary, Cable	|	190208_AB_78919b0422089833e25a1cebb1ae1fe0	|	https://www.webpagetest.org/result/190208_AB_78919b0422089833e25a1cebb1ae1fe0/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-link-preload-start-head.html	|	Dulles, Canary, Cable	|	190208_0Y_666a64306bd35e7147d4306e377b5d23	|	https://www.webpagetest.org/result/190208_0Y_666a64306bd35e7147d4306e377b5d23/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-js-inserted-link-preload.html	|	Dulles, Canary, Cable	|	190211_F3_9130e56a3f94495cb6e3b16326696ed6	|	https://www.webpagetest.org/result/190211_F3_9130e56a3f94495cb6e3b16326696ed6/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-js-inserted-link-preload-v2.html	|	Dulles, Canary, Cable	|	190211_JS_b68e87fbf3f3174a013292d3471df6e6	|	https://www.webpagetest.org/result/190211_JS_b68e87fbf3f3174a013292d3471df6e6/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-link-preload-priority-hints.html	|	Dulles, Canary, Cable	|	190211_X1_812447cb3846ba900c8ef872759eaae9	|	https://www.webpagetest.org/result/190211_X1_812447cb3846ba900c8ef872759eaae9/	|
|		|		|		|		|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-base.html	|	Dulles, Canary, 3GFast	|	190208_XB_a5262e770b59c984f1f55ece27f5ec90	|	https://www.webpagetest.org/result/190208_XB_a5262e770b59c984f1f55ece27f5ec90/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-link-preload-start-head.html	|	Dulles, Canary, 3GFast	|	190208_23_692a70978d1613fe070e16dbaf681717	|	https://www.webpagetest.org/result/190208_23_692a70978d1613fe070e16dbaf681717/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-js-inserted-link-preload.html	|	Dulles, Canary, 3GFast	|	190211_CN_996aae9613f63e778d995cff8c7c1f5a	|	https://www.webpagetest.org/result/190211_CN_996aae9613f63e778d995cff8c7c1f5a/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-js-inserted-link-preload-v2.html	|	Dulles, Canary, 3GFast	|	190211_ME_7fe9981bf31c0b78a2c86727357832ba	|	https://www.webpagetest.org/result/190211_ME_7fe9981bf31c0b78a2c86727357832ba/	|
|	https://andydavies.github.io/test-rel-preload/tests/electro/index-link-preload-priority-hints.html	|	Dulles, Canary, 3GFast	|	190211_V1_116f9fda62c36f49ff6efe27dcd50f65	|	https://www.webpagetest.org/result/190211_V1_116f9fda62c36f49ff6efe27dcd50f65/	|
|		|		|		|		|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-base.html	|	Dulles, Chrome, Cable	|	190208_8E_d8b35dd114ba6764fe2635625f9e5d67	|	https://www.webpagetest.org/result/190208_8E_d8b35dd114ba6764fe2635625f9e5d67/	|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-link-preload-start-head.html	|	Dulles, Chrome, Cable	|	190208_39_11e8f6896f70f0592983b34a95499fcc	|	https://www.webpagetest.org/result/190208_39_11e8f6896f70f0592983b34a95499fcc/	|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-js-inserted-link-preload.html	|	Dulles, Chrome, Cable	|	190212_P8_ad0478fb585299950677c43e9469c2d0	|	https://www.webpagetest.org/result/190212_P8_ad0478fb585299950677c43e9469c2d0/	|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-js-inserted-link-preload-v2.html	|	Dulles, Chrome, Cable	|	190212_BV_8db3e701f377a3cad1ccf6d20b0dff71	|	https://www.webpagetest.org/result/190212_BV_8db3e701f377a3cad1ccf6d20b0dff71/	|
|		|		|		|		|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-base.html	|	Dulles, Chrome, 3GFast	|	190208_E2_06604b7c0ec7bac81eee269b9e2fe1fc	|	https://www.webpagetest.org/result/190208_E2_06604b7c0ec7bac81eee269b9e2fe1fc/	|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-link-preload-start-head.html	|	Dulles, Chrome, 3GFast	|	190208_A3_383fa9a55c8152a108969593759ff081	|	https://www.webpagetest.org/result/190208_A3_383fa9a55c8152a108969593759ff081/	|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-js-inserted-link-preload.html	|	Dulles, Chrome, 3GFast	|	190212_6J_334d092a9dcc163c2068d504b0b2730f	|	https://www.webpagetest.org/result/190212_6J_334d092a9dcc163c2068d504b0b2730f/	|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-js-inserted-link-preload-v2.html	|	Dulles, Chrome, 3GFast	|	190212_57_1c500fb9b91c99c7a836a2f8adcd5d72	|	https://www.webpagetest.org/result/190212_57_1c500fb9b91c99c7a836a2f8adcd5d72/	|
|		|		|		|		|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-base.html	|	Dulles, Canary, Cable	|	190208_W4_30cfc6fc78fdc45b9b369e7902e1e648	|	https://www.webpagetest.org/result/190208_W4_30cfc6fc78fdc45b9b369e7902e1e648/	|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-link-preload-start-head.html	|	Dulles, Canary, Cable	|	190208_FS_5995f58791d13b3561be3bb3283c6d6e	|	https://www.webpagetest.org/result/190208_FS_5995f58791d13b3561be3bb3283c6d6e/	|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-link-preload-priority-hints.html	|	Dulles, Canary, Cable	|	190211_9A_1fab52f8315f976f18df102d3a94fed4	|	https://www.webpagetest.org/result/190211_9A_1fab52f8315f976f18df102d3a94fed4/	|
|		|		|		|		|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-base.html	|	Dulles, Canary, 3GFast	|	190208_A6_ccff5003761644d2e70e5d0fba2b17f5	|	https://www.webpagetest.org/result/190208_A6_ccff5003761644d2e70e5d0fba2b17f5/	|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-link-preload-start-head.html	|	Dulles, Canary, 3GFast	|	190208_R9_db04ccbe67cef5cb48f9cd4bfe20fe2b	|	https://www.webpagetest.org/result/190208_R9_db04ccbe67cef5cb48f9cd4bfe20fe2b/	|
|	https://test.andydavies.me/test-rel-preload/tests/electro/index-link-preload-priority-hints.html	|	Dulles, Canary, 3GFast	|	190211_MC_29f28778ed5cf6a8a7f8a02380dc5759	|	https://www.webpagetest.org/result/190211_MC_29f28778ed5cf6a8a7f8a02380dc5759/	|
|		|		|		|		|
|	https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-base.html	|	Dulles, Chrome, Cable	|	190209_9Z_b778e6415fec5e9764f9a6ec8a0bb8b2	|	https://www.webpagetest.org/result/190209_9Z_b778e6415fec5e9764f9a6ec8a0bb8b2/	|
|	https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-link-preload-start-head.html	|	Dulles, Chrome, Cable	|	190209_24_97bdcc36271819abc3adbcad163650cd	|	https://www.webpagetest.org/result/190209_24_97bdcc36271819abc3adbcad163650cd/	|
|		|		|		|		|
|	https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-base.html	|	Dulles, Chrome, 3GFast	|	190209_AP_6edfa5e21de919c946c7bd529ab10160	|	https://www.webpagetest.org/result/190209_AP_6edfa5e21de919c946c7bd529ab10160/	|
|	https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-link-preload-start-head.html	|	Dulles, Chrome, 3GFast	|	190209_PQ_bd29c967a27f87c9d162a5e7c2c584e3	|	https://www.webpagetest.org/result/190209_PQ_bd29c967a27f87c9d162a5e7c2c584e3/	|
|		|		|		|		|
|	https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-base.html	|	Dulles, Canary, Cable	|	190209_K0_340ff3306812d4354a49264b5fc2bc9f	|	https://www.webpagetest.org/result/190209_K0_340ff3306812d4354a49264b5fc2bc9f/	|
|	https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-link-preload-start-head.html	|	Dulles, Canary, Cable	|	190209_H3_6af5caea1277011adfcdf7c608dacd5e	|	https://www.webpagetest.org/result/190209_H3_6af5caea1277011adfcdf7c608dacd5e/	|
|	https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-link-preload-priority-hints.html	|	Dulles, Canary, Cable	|	190211_N4_756347536f145f415484f6aa05c1b74f	|	https://www.webpagetest.org/result/190211_N4_756347536f145f415484f6aa05c1b74f/	|
|		|		|		|		|
|	https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-base.html	|	Dulles, Canary, 3GFast	|	190209_24_ecf83b17f580ee952d641d8def6523ee	|	https://www.webpagetest.org/result/190209_24_ecf83b17f580ee952d641d8def6523ee/	|
|	https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-link-preload-start-head.html	|	Dulles, Canary, 3GFast	|	190209_5P_0adf414acd63b1067b6f20e7d200795b	|	https://www.webpagetest.org/result/190209_5P_0adf414acd63b1067b6f20e7d200795b/	|
|	https://d1mqs4cikzff9z.cloudfront.net/test-rel-preload/tests/electro/index-link-preload-priority-hints.html	|	Dulles, Canary, 3GFast	|	190211_ZD_4e9f11afce2229cfbc22bb769d8ede36	|	https://www.webpagetest.org/result/190211_ZD_4e9f11afce2229cfbc22bb769d8ede36/	|