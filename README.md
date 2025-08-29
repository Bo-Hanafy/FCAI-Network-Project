# 📡 مشروع شبكات - امتحان عملي  

## 📌 فكرة المشروع  
المشروع ده كان عبارة عن بناء شبكة متقدمة باستخدام **Cisco Packet Tracer**.  
الفكرة كانت إننا نعمل VLANs لأقسام مختلفة (زي HR، IT، Management...)، والأقسام دي تشوف بعض عن طريق **Inter-VLAN Routing**.  
كمان كل جهاز في الشبكة بياخد IP بشكل **Dynamic** من خلال **DHCP Server**، ومعانا كمان **DNS Server** عشان الأجهزة تقدر تعمل Ping على أسماء مواقع زي:  
```bash
ping google.com
ping hunter.com
🛠️ المكونات اللي استخدمتها ##
عدد من أجهزة الكمبيوتر (PCs) موزعين على VLANs مختلفة.

Switches (من نوع Layer 3) لتقسيم VLANs والتوجيه بينهم.

Router (Router Model: 2911 للربط بين الشبكات المختلفة).

DHCP Server لتوزيع عناوين IP بشكل ديناميكي.

DNS Server لحل أسماء الدومين (Name Resolution).

كابلات للتوصيل:

كابلات عادية (Copper Straight-Through) بين الـ PCs والسويتشات.

كابلات عادية برضه بين Switches Layer 3 والـ Routers.

كابلات Serial (مثلاً Serial 0/0/0) لما وصلت Router براوتر.
##⚙️ خطوات التنفيذ
عملت VLANs لكل قسم ووزعت الأجهزة عليهم.

خصصت لكل Port على السويتش VLAN معينة.

فعلت Router on a Stick وربطت كل VLAN بـ Sub-Interface على الراوتر.

جهزت DHCP Server وخصصت Pools مختلفة لكل VLAN.

ضفت DNS Server وسجلت فيه أسماء دومينات (زي google.com و hunter.com).

عملت التوصيلات كالتالي:

PC → Switch (Layer 3) باستخدام كابل Straight.

Switch → Router باستخدام كابل Straight.

Router → Router باستخدام كابل Serial (0/0/0).

جربت Ping داخلي بين VLANs مختلفة للتأكد من إن الـ Routing شغال.

جربت كمان Ping على الدومينات للتأكد إن الـ DNS شغال
##✅ النتيجة
كل VLAN قدرت تشوف التانية.

الأجهزة أخدت IPs ديناميكي من الـ DHCP Server.

الـ DNS Server حل أسماء الدومينات بشكل سليم.

الـ Ping اشتغل على المواقع المسجلة زي google.com و hunter.com.

المشروع اتنفذ بنجاح وحقق المطلوب في الامتحان.
##💡 نصائح للمذاكرة
ذاكروا كويس جدًا أسئلة Routing والبروتوكولات (RIP, OSPF, EIGRP...).

احفظوا اختصارات البروتوكولات كويس، الأسئلة بتيجي مباشرة فيها.

راجعوا على الـ OSI Model والـ TCP/IP Model لأنهم أساس الفهم.




