#Jennifer Kwon

""" Before using this function, you must use the neo4j driver for Python. Refer to Neo4jDriver.py.

  After exporting the style.grass file from neo4j, run this function on a Python IDE and pass 
  node_label: "Topic", new_node_color: "#FFB6C1", node_style_property: "color" as parameters.
  In your directory, file new_style.grass will be created and you must manually import it onto neo4j.
 
"""

def change_color_of_node(self, node_label: str, new_node_color: str, node_style_property: str):

        new_node_label = "node." + node_label
        with open("style.grass", 'r', newline="") as file_object:

            nodes_styles = file_object.readlines()
            
        with open("new_style.grass", 'w') as file_object_2:
                
            i = 0
            while i < len(nodes_styles):

                if node_label in nodes_styles[i]:
                        
                    file_object_2.write(nodes_styles[i])
                        
                    if node_style_property not in nodes_styles[i]:

                        i+=1
                            
                    if node_style_property in nodes_styles[i]:
                        
                        old_node_color = nodes_styles[i][9:16]
                        
                        new_string = nodes_styles[i].replace(old_node_color, new_node_color)
                        
                        file_object_2.write(new_string)
                        i+=1
                else:
                    file_object_2.write(nodes_styles[i]) 
                    i+=1
                    
        return
