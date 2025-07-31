<img width="1696" height="214" alt="image" src="https://github.com/user-attachments/assets/73d9a9bf-29fa-4bb1-b368-c62305547efa" />
通过RQ-VAE学习码本，为每个item分配一个语义id，并且最后第四位加一个。如果只有独立一个item,则第四位是0，否则就是0，1，2往上加
loss为：即重建损失跟每个码本跟输入的embedding的距离。 <img width="1738" height="124" alt="image" src="https://github.com/user-attachments/assets/00ad3fbf-8b79-4e30-9198-fdf257d74e86" />

<img width="1724" height="846" alt="image" src="https://github.com/user-attachments/assets/1193b29f-b202-40c2-b91e-5a4750bf515a" />
他说通过检索的方式拿到id的，而不是softmax。输出的embedding,直接去码本里面检索。通过压缩码本空间，可以提高命中率。
、
、

<img width="1922" height="950" alt="image" src="https://github.com/user-attachments/assets/041ce820-0bc6-4bf2-bb52-3ead277bcc84" />
k-means存在这个问题的。只是局部最优。RQVAE通过动态训练embedding，可以改善
