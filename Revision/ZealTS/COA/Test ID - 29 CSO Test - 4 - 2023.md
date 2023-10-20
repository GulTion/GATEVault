---
atQ: 15
type: ZealTS
subject: COA
subType: topicWise
last_time: 2023-10-20T00:00:00.000+05:30
syllabus: Advanced Pipeline Concept, I/O Interface(Interrupt And DMA), ALU, Data-Path And Control Unit
startQ: 1
endQ: 25
status: Analysis
repeation: 3
src: https://uxkhzfstdjcborfuyyknhkhbyfnskrywvveioufkbjkupomnptjwvhbavkysuhi.vercel.app/solution.html?testId=62cea705550abd866f9de327&test_id=25
---
#card/COA
- 3 ![[Pasted image 20231015145010.png]]::![[Pasted image 20231015145019.png]]
- 4. ![[Pasted image 20231015145834.png]]::![[Pasted image 20231015145841.png]]
- 8. ![[Pasted image 20231015152151.png]]::![[Pasted image 20231015152158.png]]
- 9. ![[Pasted image 20231015152624.png]]::![[Pasted image 20231015152632.png]]
- 10. ![[Pasted image 20231015153753.png]]::![[Pasted image 20231015153805.png]]
- 11. ![[Pasted image 20231020145351.png]]::this will not provide the opretor forwarding bcz, for forwading the data of register must be flow from WB=>PO(EX). but in question the gave WB=>ID, so that's why, this will create extra stall![[Pasted image 20231020145400.png]]
- 13.  ![[Pasted image 20231020151953.png]]::find any intruction into the loop that is independent so that we can put it at the end of the branching so that we can avoid the stall, if can't find in loop then find **outside of loop**, who didn't depend on any other instruction![[Pasted image 20231020152012.png]]