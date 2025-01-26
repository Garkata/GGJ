using UnityEngine;

public class TeleportInteraction : MonoBehaviour
{
    public GameObject player;
    public float interactionRange = 5f;

    
    private Vector2 teleportPosition = new Vector2(-24, -1);

    private void Update()
    {
        
        if (Input.GetMouseButtonDown(0)) 
        {
            
            Vector2 mousePosition = Camera.main.ScreenToWorldPoint(Input.mousePosition);

            
            if (IsMouseOverSprite(mousePosition))
            {
                TryTeleport();
            }
        }
    }

   
    private bool IsMouseOverSprite(Vector2 mousePosition)
    {
       
        float distance = Vector2.Distance(transform.position, mousePosition);

        
        return distance <= 0.5f; 
    }

   
    private void TryTeleport()
    {
        
        float distance = Vector2.Distance(player.transform.position, transform.position);

      
        if (distance <= interactionRange)
        {
            player.transform.position = teleportPosition;
            Debug.Log("Player teleported to: " + teleportPosition);
        }
        else
        {
            Debug.Log("Player is too far from the sprite.");
        }
    }
}
