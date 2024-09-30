Zenith
zenithtsu
Though it may hurt today, tomorrow I'll be heading my way

Nicholas Van Lukman — 05/11/2023 17:38
Kalau statistik udah gw mau lihat yaa wkwkwkw
Perlu sources tambahann
Zenith — 05/11/2023 17:44
Attachment file type: acrobat
Catatan_Basic_Statistik.pdf
5.47 MB
w ga nyatet yang sesi 4 5 6
Nicholas Van Lukman — 05/11/2023 19:48
Ah okeokee
Thank You Broo
Nicholas Van Lukman — 05/12/2023 23:49
Attachment file type: document
KomodoSense_Decoy.pptx
323.13 KB
Zenith — 27/09/2024 16:58
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.EventSystems;

public class CardMovementAttemp : MonoBehaviour//, IDragHandler//, IBeginDragHandler, IEndDragHandler
Expand
message.txt
5 KB
Nicholas Van Lukman — 27/09/2024 17:10
if (Input.GetMouseButtonDown(1))
    {
        Ray ray = Camera.main.ScreenPointToRay(Input.mousePosition);
        RaycastHit hit;

        if (Physics.Raycast(ray, out hit))
        {
            if (hit.collider.gameObject == gameObject && proceedCaroutine)
            {
                StartCoroutine(CardRotation());
            }
}
}
Nicholas Van Lukman — 27/09/2024 17:25
if (Input.GetMouseButtonDown(1))
    {
        Vector2 mousePos = Camera.main.ScreenToWorldPoint(Input.mousePosition);
        RaycastHit2D hit = Physics2D.Raycast(mousePos, Vector2.zero);

        if (hit.collider != null && hit.collider.gameObject == gameObject && proceedCaroutine)
        {
            StartCoroutine(CardRotation());
        }
    }
}
Nicholas Van Lukman — 27/09/2024 17:42
private IEnumerator CardRotation()
{
    proceedCaroutine = false;

    if (card.cardData.cardPosition == CardPosition.Up)
    {
        for (float i = 0f; i <= 180f; i += 10f)
        {
            transform.rotation = Quaternion.Euler(0f, i, 0f);

            // Reset the collider bounds (for 2D physics)
            GetComponent<BoxCollider2D>().enabled = false;
            GetComponent<BoxCollider2D>().enabled = true;

            if (i == 90f)
            {
                card.cardData.cardPosition = CardPosition.Down;
                cardUI.backNumber.transform.rotation = Quaternion.Euler(0f, -i, 0f);
            }
            yield return new WaitForSeconds
else if (card.cardData.cardPosition == CardPosition.Down)
    {
        for (float i = 180f; i >= 0f; i -= 10f)
        {
            transform.rotation = Quaternion.Euler(0f, i, 0f);

            // Reset the collider bounds (for 2D physics)
            GetComponent<BoxCollider2D>().enabled = false;
            GetComponent<BoxCollider2D>().enabled = true;

            if (i == 90f)
            {
                card.cardData.cardPosition = CardPosition.Up;
            }
            yield return new WaitForSeconds(0.01f);
        }
    }

    proceedCaroutine = true;
}
Zenith — Yesterday at 19:15
wah bener w co
kartunya ga kedetect klo y axis nya -
w ubah rotasinya jadi selalu mulai dari 180 ke 0, sekarang langsung bisa didrag ;v
Nicholas Van Lukman — Yesterday at 22:22
Wthhhh?
Unity ada fitur seperti itu damn
Kalau mulai dari 0 kaya kemarin rotasinya ga bisaa?
Zenith — Yesterday at 22:22
bukan karna - deh ;v
ternyata klo axis y nya lebih dari 0 jadi gabisa dipencet
lebih parah ;v
Nicholas Van Lukman — Yesterday at 22:23
Ohhhhh
Perhaps dia anggapnya jadi bukan game object
Incase dibawah 0 yaitu mines :/ 
Tapi sekarang dah bisaa?
Zenith — Yesterday at 22:23
ye
Nicholas Van Lukman — Yesterday at 22:24
IPointerEnterHandler masih kepake?
atau lu ada teknik lain?
Zenith — Yesterday at 22:24
yoi
ga kepikiran cara lain w
Nicholas Van Lukman — Yesterday at 22:24
Wkwkkwwk make senses
Kemarin lihat game 10 days to die ga?
Renala Games lihat ga?
Zenith — Yesterday at 22:25
10 days to die liat
renala yg mana?
Nicholas Van Lukman — Yesterday at 22:25
Depannya 10 days to die
Zenith — Yesterday at 22:25
helen?
Nicholas Van Lukman — Yesterday at 22:25
Noo
Itu sampingnya renala games
But intinya both have crafting system
Dan cara mouse mereka focus ke satu object itu yaitu slot istilahnya
Pake IPointerEnterHandler juga
Gw tanya tanya pas Jadi peserta palsu wkwkwkwkkw
Zenith — Yesterday at 22:26
bjir ;v
Nicholas Van Lukman — Yesterday at 22:26
Gw penasaran cara lain si
Masa ini doang wkwkkwkwk
Raycast not working juga kemarin :/
Sekarang ada problem lagi ga di programming?
TurnBaseManager gitu? atau apa
Nicholas Van Lukman — Today at 15:51
# Hi, I'm Nicholas Van Lukman
---
Nice to meet you! I'm currently a student at Bina Nusantara University, majoring in Game Application and Technology. </br>
I do game programming and various aspect of game development due to my versatility. </br>
You can check and download games I've developed at (https://bisniskomodo.itch.io/)
Expand
message.txt
6 KB
﻿
Nicholas Van Lukman
nicholasvan
 
 
My Shop : https://www.tokopedia.com/bisniskomodo
# Hi, I'm Nicholas Van Lukman
---
Nice to meet you! I'm currently a student at Bina Nusantara University, majoring in Game Application and Technology. </br>
I do game programming and various aspect of game development due to my versatility. </br>
You can check and download games I've developed at (https://bisniskomodo.itch.io/)

*All the GIFs are linked to their respective itch.io page*

# Here are highlights from some of the games I made:
<table width="100%">
  <thead>
    <tr>
      <th width="50%"><a href="https://bisniskomodo.itch.io/">Sive 2</a></th>
      <th width="50%"><a href="https://bisniskomodo.itch.io/please-survive">Please Survive</a></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/735f704f-0539-455a-8a75-d8300dac3b22"/>
   </td>
      <td><img src="https://github.com/user-attachments/assets/06147d37-3902-4eaa-a851-ca548fae0fba"/>
   </td>
    </tr>
    <tr>
      <td valign="text-top">Sive 2, depicting a vast survival game where you need to manage your hunger and thirst to continue your journey. You objective is Hunt for your survivability and  to escape the dangerous island. I forged the HUD, inventory system, hotbar shortcut, Drag and drop handler, Slot generator, Item scriptable object, and also created the terrain.</td>
      <td valign="text-top"">Please Survive, 2D top down shooter that rush yourself to a zombie apocalypse that keep spawning. You gotta kill them in order to survive the world. Each kills grant you score that makes the game even harder. I formulated a simple zombie enemy behavior, shooting scripts, Scoring system, animation system, gun system, and also the Healthcontroller.<div></div></td>
    </tr>
    <tr>
      <td><b>Types : Solo Developer</br>Contribution : Game Programmer</b></td>
      <td><b>Types : Solo Developer</br>Contribution : Game Programmer</b></td>
    </tr>
    <tr>
      <td><a href="https://bisniskomodo.itch.io/">Itch Page</td>
      <td><a href="https://bisniskomodo.itch.io/please-survive">Itch Page</td>
    </tr>
  </tbody>
</table>

<br>

<table width="100%">
  <thead>
    <tr>
      <th width="50%"><a href="https://bisniskomodo.itch.io/lightning-boy">Lightning Boy</a></th>
      <th width="50%"><a href="https://bisniskomodo.itch.io/wee-land">WEE Land</a></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/fb2d68c9-ced2-4645-ae55-993a4fe72207"/>
     </td>
      <td><img src="https://github.com/user-attachments/assets/d3e103ab-ea0f-43bd-8266-791af05a8f1c"/>
   </td>
    </tr>
    <tr>
      <td valign="text-top">Lightning boy remains as my first simple game, inspired by Super Mario Bros where you gotta jump and avoid obstacle in order to reach to your winning places. I built the player movement system,  Climbing System, Healthcontroller and the kill system for the player when falling to lava or touch nearby obstacle.</td>
      <td valign="text-top">WEE Land is a game that entirely forgoes combat system. Your main objective is to survive as long as possible maintaining the Welfare, Entertainment and Education meter for the citizen. You are given a limited budget to satisfy the need of the citizen. I create Citizen meter, Shop System, Budget system, Day system, Next day system and a random event which trigger every one day.<br></td>
    </tr>
    <tr>
      <td><b>Types : Solo Developer</br>Contribution : Game Programmer</b></td>
      <td><b>Types : Team Group</br>Contribution : Game Programmer</b></td>
    </tr>
    <tr>
      <td><a href="https://bisniskomodo.itch.io/lightning-boy">Itch Page</td>
      <td><a href="https://bisniskomodo.itch.io/wee-land">Itch Page</td>
    </tr>
  </tbody>
</table>

<table width="100%">
  <thead>
    <tr>
      <th width="50%"><a href="https://xviig.itch.io/echoes-beneath">Echoes Beneath</a></th>
      <th width="50%"><a href="https://bisniskomodo.itch.io/">Nightwalker</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/2b7225fe-1086-456b-917a-7137fba4ecec"/>
   </td>
      <td><img src="https://github.com/user-attachments/assets/b909409e-58b4-412f-9299-65c7fd2fa245"/>
   </td>
    </tr>
    <tr>
      <td valign="text-top">Echoes beneath is a 3D First Person Horror in which the players will experience a one of a kind journey traversing the depths of a sewer beneath France. Your main objective as the sewer worker is to repair leaking pipes and generators. I animated the character movement, crouch, monster chase, jumpscares and also created sound effect for the game.</td>
      <td valign="text-top">Nightwalkers is a 2D platformer with punishing opponents as its main mechanic. Taking place in a near modern day future. You play as Luna, a nightwalker with your trusty katana, slashing enemies and parrying their attacks while exploring the beautiful yet mysterious city.I created character attack combo, parry animation, and sound effect for the game.<br></td>
    </tr>
    <tr>
      <td><b>Types : Game Jam</br>Contribution : Animator and Sound Engineer</b></td>
      <td><b>Types : Game Jam</br>Contribution : Animator and Sound Engineer</b></td>
    </tr>
    <tr>
      <td><a href="https://xviig.itch.io/echoes-beneathy">Itch Page</td>
      <td><a href="https://bisniskomodo.itch.io/">Itch Page</td>
    </tr>
  </tbody>
</table>
message.txt
6 KB
