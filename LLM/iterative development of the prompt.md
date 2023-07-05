---
type: Coding  
tags: llm ,prompt
category: work
for_inteview: True
creation_date: 2023-07-05 15:42
modification_date: 2023-07-05 15:42
---

  
Current Folder : LLM




[[05-07-2023]]


It is very much unlikely to happen that , we will find our optimum or final prompt in the very first try. We need to use simple prompt first, the, find out the limitation , and improving the prompt by analyzing the limitations. 

![[Pasted image 20230705155606.png]]

![[Pasted image 20230705155630.png]]

a basic prompt can be ![[Pasted image 20230705155700.png]]
![[Pasted image 20230705155726.png]]

the very first issue of this prompt is the model is outputting too much text. we need to improve the prompt by specifying the text limit. 
![[Pasted image 20230705155826.png]]

now , we may find out , that , the output has focused on wrong information. the indented audience might be different . so , we must improve the prompt by including that. 
![[Pasted image 20230705160305.png]]

if we want to inject any additional information , we can do that as well
![[Pasted image 20230705160445.png]]

lastly , we can ask the model to format the output in specific order and structure ![[Pasted image 20230705160559.png]]

```html
<div>
  <h2>Product Description</h2>
  <p>
    Introducing our latest addition to our mid-century inspired office furniture collection - the SWC Chair. This chair is part of a beautiful family of furniture that includes filing cabinets, desks, bookcases, meeting tables, and more. With its sleek design and customizable options, the SWC Chair is the perfect choice for any home or business setting.
  </p>
  <p>
    The SWC Chair offers several options for customization. You can choose from a variety of shell colors and base finishes to match your existing decor. The chair is available with either plastic back and front upholstery or full upholstery in a range of fabric and leather options. The base finish options include stainless steel, matte black, gloss white, or chrome. You can also choose whether to have armrests or not, depending on your preference.
  </p>
  <p>
    The construction of the SWC Chair is top-notch. It features a 5-wheel plastic coated aluminum base, ensuring stability and durability. The chair also has a pneumatic adjuster, allowing for easy raise and lower action. This makes it convenient for users to find their desired height and maintain proper posture throughout the day.
  </p>
  <p>
    The SWC Chair is designed with comfort in mind. The seat is made with HD36 foam, providing a plush and supportive cushioning experience. You can also choose between soft or hard-floor caster options, depending on the type of flooring in your space. Additionally, there are two choices of seat foam densities available: medium (1.8 lb/ft3) or high (2.8 lb/ft3). This allows you to customize the level of firmness to suit your preferences.
  </p>
  <p>
    The SWC Chair is not only stylish and comfortable, but it is also built to last. The shell base glider is made of cast aluminum with a modified nylon PA6/PA66 coating, ensuring strength and durability. The shell has a thickness of 10 mm, providing stability and support. With its high-quality materials and construction, the SWC Chair is qualified for contract use, making it suitable for commercial settings as well.
  </p>
  <p>
    The SWC Chair is proudly made in Italy, known for its craftsmanship and attention to detail. With its timeless design and customizable options, this chair is sure to enhance any space, whether it's a home office or a corporate environment.
  </p>
  <h2>Product Dimensions</h2>
  <table>
    <tr>
      <th>Dimension</th>
      <th>Measurement (inches)</th>
    </tr>
    <tr>
      <td>Width</td>
      <td>20.87"</td>
    </tr>
    <tr>
      <td>Depth</td>
      <td>20.08"</td>
    </tr>
    <tr>
      <td>Height</td>
      <td>31.50"</td>
    </tr>
    <tr>
      <td>Seat Height</td>
      <td>17.32"</td>
    </tr>
    <tr>
      <td>Seat Depth</td>
      <td>16.14"</td>
    </tr>
  </table>
</div>

Product IDs: SWC-100, SWC-110

```

we can see the usage 
![[Pasted image 20230705160638.png]]

