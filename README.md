 Esp ไปเเย่งกันเอง มีเขียนจำเเนกใว้ 
  
  function isnil(thing)
	 return (thing == nil)
  end
  local function round(n)
	 return math.floor(tonumber(n) + 0.5)
  end
  Number = math.random(1, 1000000)
  function UpdatePlayerChams()
	 for i,v in pairs(game:GetService'Players':GetChildren()) do
		pcall(function()
			  if not isnil(v.Character) then
				 if ESPPlayer then
					if not isnil(v.Character.Head) and not v.Character.Head:FindFirstChild('NameEsp'..Number) then
					local bill = Instance.new('BillboardGui',v.Character.Head)
					bill.Name = 'NameEsp'..Number
					bill.ExtentsOffset = Vector3.new(0, 1, 0)
					bill.Size = UDim2.new(1,200,1,30)
					bill.Adornee = v.Character.Head
					bill.AlwaysOnTop = true
					local name = Instance.new('TextLabel',bill)
					name.Font = "GothamBold"
					name.FontSize = "Size14"
					name.TextWrapped = true
					name.Text = (v.Name ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M')
					name.Size = UDim2.new(1,0,1,0)
					name.TextYAlignment = 'Top'
					name.BackgroundTransparency = 1
					name.TextStrokeTransparency = 0.5
					if v.Team == game.Players.LocalPlayer.Team then
						  name.TextColor3 = Color3.fromRGB(73, 255, 0)
					else
						  name.TextColor3 = Color3.fromRGB(255,10, 0)
					end
					else
						  v.Character.Head['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M')
					end
				 else
					if v.Character.Head:FindFirstChild('NameEsp'..Number) then
					v.Character.Head:FindFirstChild('NameEsp'..Number):Destroy()
					end
				 end
			  end
		end)
	 end
  end
  function UpdateChestChams()
	 for i,v in pairs(game.Workspace:GetChildren()) do
		pcall(function()
			  if string.find(v.Name,"Chest") then
				 if ChestESP then
					if string.find(v.Name,"Chest") then
						  if not v:FindFirstChild('NameEsp'..Number) then
							 local bill = Instance.new('BillboardGui',v)
							 bill.Name = 'NameEsp'..Number
							 bill.ExtentsOffset = Vector3.new(0, 1, 0)
							 bill.Size = UDim2.new(1,200,1,30)
							 bill.Adornee = v
							 bill.AlwaysOnTop = true
							 local name = Instance.new('TextLabel',bill)
							 name.Font = "GothamBold"
							 name.FontSize = "Size14"
							 name.TextWrapped = true
							 name.Size = UDim2.new(1,0,1,0)
							 name.TextYAlignment = 'Top'
							 name.BackgroundTransparency = 1
							 name.TextStrokeTransparency = 0.5
							 if v.Name == "Chest1" then
								name.TextColor3 = Color3.fromRGB(255, 10, 0)
								name.Text = ("Chest 1" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
							 end
							 if v.Name == "Chest2" then
								name.TextColor3 = Color3.fromRGB(73, 255, 0)
								name.Text = ("Chest 2" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
							 end
							 if v.Name == "Chest3" then
								name.TextColor3 = Color3.fromRGB(255,191, 0)
								name.Text = ("Chest 3" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
							 end
						  else
							 v['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
						  end
					end
				 else
					if v:FindFirstChild('NameEsp'..Number) then
					v:FindFirstChild('NameEsp'..Number):Destroy()
					end
				 end
			  end
		end)
	 end
  end
  function UpdateDevilChams()
	 for i,v in pairs(game.Workspace:GetChildren()) do
		pcall(function()
			  if DevilFruitESP then
				 if string.find(v.Name, "Fruit") then
					if not v.Handle:FindFirstChild('NameEsp'..Number) then
						  local bill = Instance.new('BillboardGui',v.Handle)
						  bill.Name = 'NameEsp'..Number
						  bill.ExtentsOffset = Vector3.new(0, 1, 0)
						  bill.Size = UDim2.new(1,200,1,30)
						  bill.Adornee = v.Handle
						  bill.AlwaysOnTop = true
						  local name = Instance.new('TextLabel',bill)
						  name.Font = "GothamBold"
						  name.FontSize = "Size14"
						  name.TextWrapped = true
						  name.Size = UDim2.new(1,0,1,0)
						  name.TextYAlignment = 'Top'
						  name.BackgroundTransparency = 1
						  name.TextStrokeTransparency = 0.5
						  name.TextColor3 = Color3.fromRGB(73, 255, 0)
						  name.Text = (v.Name ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude/3) ..' M')
					else
						  v.Handle['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude/3) ..' M')
					end
				 end
			  else
				 if v.Handle:FindFirstChild('NameEsp'..Number) then
					v.Handle:FindFirstChild('NameEsp'..Number):Destroy()
				 end
			  end
		end)
	 end
  end
  function UpdateFlowerChams()
	 for i,v in pairs(game.Workspace:GetChildren()) do
		pcall(function()
			  if v.Name == "Flower2" or v.Name == "Flower1" then
				 if FlowerESP then
					if not v:FindFirstChild('NameEsp'..Number) then
						  local bill = Instance.new('BillboardGui',v)
						  bill.Name = 'NameEsp'..Number
						  bill.ExtentsOffset = Vector3.new(0, 1, 0)
						  bill.Size = UDim2.new(1,200,1,30)
						  bill.Adornee = v
						  bill.AlwaysOnTop = true
						  local name = Instance.new('TextLabel',bill)
						  name.Font = "GothamBold"
						  name.FontSize = "Size14"
						  name.TextWrapped = true
						  name.Size = UDim2.new(1,0,1,0)
						  name.TextYAlignment = 'Top'
						  name.BackgroundTransparency = 1
						  name.TextStrokeTransparency = 0.5
						  name.TextColor3 = Color3.fromRGB(255, 0, 0)
						  if v.Name == "Flower1" then
							 name.Text = ("Blue Flower" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
							 name.TextColor3 = Color3.fromRGB(255,10,0)
						  end
						  if v.Name == "Flower2" then
							 name.Text = ("Red Flower" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
							 name.TextColor3 = Color3.fromRGB(0, 12, 255 )
						  end
					else
						  v['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
					end
				 else
					if v:FindFirstChild('NameEsp'..Number) then
					v:FindFirstChild('NameEsp'..Number):Destroy()
					end
				 end
			  end
		end)
	 end
  end
  
  Raids:Toggle("ESP Player","",_G.Save["ESPPlayer"],function(a)
	 ESPPlayer = a
	 _G.Save["ESPPlayer"] = a 
	 SaveSetting()
	 while ESPPlayer do wait()
		UpdatePlayerChams()
	 end
  end)
  Raids:Toggle("ESP Chest","",_G.Save["ESPChest"],function(a)
	 ChestESP = a
	 _G.Save["ESPChest"] = a
	 SaveSetting()
	 while ChestESP do wait()
		UpdateChestChams()
	 end
  end)
  Raids:Toggle("ESP Devil Fruit","",_G.Save["ESPDevil"],function(a)
	 DevilFruitESP = a
	 _G.Save["ESPDevil"] = a
	 SaveSetting()
	 while DevilFruitESP do wait()
		UpdateDevilChams()
	 end
  end)
  Raids:Toggle("ESP Flower","",_G.Save["ESPFlower"],function(a)
	 FlowerESP = a
	 _G.Save["ESPFlower"] = a 
	 SaveSetting()
	 while FlowerESP do wait()
		UpdateFlowerChams()
	 end
  end)
  
  อธิบายภาษา
  Course Programming

Lua เผื่อคุณยังไม่รู้ มันคือภาษาโปรแกรมภาษานึงแหละ ที่เป็นแบบแปลคำสั่งแล้วทำงานเป็นบรรทัดๆไป โดยไม่ต้องคอมไพล์และแปลให้เป็นภาษาเครื่องก่อน จุดเด่นของมันก็คือเร็วส์ ยืดหยุ่น ง่าย และไม่ยากในการศึกษา (ไม่ใช่อันเดียวกันกับ “ง่าย” เหรอ)

สิ่งที่จำเป็นต้องรู้เกี่ยวกับภาษา Lua อย่างเช่น รูปแบบคำสั่ง โอเปอเรเตอร์ ฟังก์ชันต่างๆ

ตัวแปรและประเภทของตัวแปร

ก็เหมือนกับภาษาแบบสคริปต์โดยทั่วไป คือ มันไม่มีชนิดของตัวแปรหรอก แปลว่าเราสามารถตั้งค่าให้ตัวแปรได้เลย อย่างเช่น
var = value
แต่มันก็มีการตั้งค่าให้แบบ global และ local นะ เหมือนภาษาอื่นๆแหละ แถมเราตั้งค่าให้มันทั้งหมดในรวดเดียวแบบนี้ได้เลย

คำสงวนที่ต้องระวัง ในภาษา Lua มีคำสงวนที่ต้องระวังในการใช้ คำพวกนี้ก็มี nil ซึ่งหมายถึงทั้งตัวแปรที่ไม่ได้ตั้งค่า (undefined) และตัวแปรที่ไม่มีค่า (null) อีกคำสงวนคือ false และ true เวลาใช้ false ใน statement ให้ระวังเพราะใน Lua มีแค่ 2 อันที่เท่ากับ false คือ nil กับ false ที่เหลือทั้งหมดคือ true

ลัวะคืออะไร?
Lua เป็นภาษาสคริปต์แบบฝังได้ที่ทรงพลัง มีประสิทธิภาพ น้ำหนักเบา รองรับการตั้งโปรแกรมตามขั้นตอน การเขียนโปรแกรมเชิงวัตถุ การเขียนโปรแกรมเชิงฟังก์ชัน การเขียนโปรแกรมที่ขับเคลื่อนด้วยข้อมูล และคำอธิบายข้อมูล

Lua รวมไวยากรณ์ขั้นตอนง่าย ๆ เข้ากับโครงสร้างคำอธิบายข้อมูลที่มีประสิทธิภาพตามอาร์เรย์ที่เชื่อมโยงและความหมายที่ขยายได้ Lua ถูกพิมพ์แบบไดนามิก ทำงานโดยการตีความ bytecode ด้วยเครื่องเสมือนแบบลงทะเบียน และมีการจัดการหน่วยความจำอัตโนมัติพร้อมการรวบรวมขยะที่เพิ่มขึ้น ทำให้เหมาะสำหรับการกำหนดค่า การเขียนสคริปต์ และการสร้างต้นแบบอย่างรวดเร็ว

ลัวะมาจากไหน?
Lua ได้รับการออกแบบ ใช้งาน และดูแลโดยทีมงานที่ PUC-Rio ซึ่งเป็นมหาวิทยาลัย Pontifical Catholic University of Rio de Janeiro ในบราซิล Lua เกิดและเติบโตใน Tecgraf ซึ่งเดิมคือกลุ่มเทคโนโลยีกราฟิกคอมพิวเตอร์ของ PUC-Rio ปัจจุบัน Lua ตั้งอยู่ที่ LabLua ซึ่งเป็นห้องปฏิบัติการของภาควิชาวิทยาการคอมพิวเตอร์ของ PUC-Rio

อยู่ในชื่ออะไร?
"ลั่ว" (ออกเสียงว่า "ห-อา") หมายถึง "ดวงจันทร์" ในภาษาโปรตุเกส ดังนั้น จึงไม่ใช่คำย่อหรือตัวย่อ แต่เป็นคำนาม โดยเฉพาะอย่างยิ่ง "ลัวะ" คือชื่อ ดวงจันทร์ของโลก และชื่อภาษา เช่นเดียวกับชื่ออื่นๆ ควรเขียนด้วยตัวพิมพ์เล็กด้วยอักษรตัวพิมพ์ใหญ่เริ่มต้น นั่นคือ "ลัวะ" โปรดอย่าเขียนเป็น "LUA" ซึ่งทั้งน่าเกลียดและน่าสับสน เพราะมันจะกลายเป็นคำย่อที่มีความหมายต่างกันสำหรับแต่ละคน ดังนั้นโปรดเขียน "ลัวะ" ให้ถูกต้อง!

เข้าร่วมชุมชน
มีจุดนัดพบหลายแห่งสำหรับชุมชน Lua ที่คุณสามารถไปเรียนรู้และช่วยเหลือผู้อื่นและมีส่วนร่วมด้วยวิธีอื่นๆ ประเด็นสำคัญประการหนึ่งคือรายชื่อผู้รับจดหมายซึ่งมีความกระตือรือร้นและเป็นมิตร

คุณสามารถพบกับส่วนหนึ่งของชุมชน Lua ด้วยตนเองโดยเข้าร่วม Lua Workshop
สนับสนุน Lua
คุณสามารถช่วยสนับสนุนโครงการ Lua โดยการซื้อหนังสือที่เผยแพร่โดย Lua.org และโดยการบริจาค

คุณสามารถช่วยกระจายข่าวเกี่ยวกับ Lua ได้โดยการซื้อผลิตภัณฑ์ Lua ที่ Zazzle

Lua.org เป็น Amazon Associate และเราได้รับค่าคอมมิชชั่นสำหรับการซื้อที่เข้าเงื่อนไขผ่านลิงก์ในไซต์นี้

ภาษา C++

ในบทเรียนนี้ คุณจะได้เรียนเกี่ยวกับภาษา C++ เราจะแนะนำคุณให้รู้จักกับภาษา C++ และโครงสร้างพื้นฐานของภาษา เช่น ตัวแปร ตัวดำเนินการ อาเรย์ คำสั่งควบคุม โครงสร้างข้อมูล พอยน์เตอร์ และอื่นๆ นอกจากนี้เรายังจะพูดถึงการเขียนโปรแกรมเชิงวัตถุ ซึ่งเป็นคุณสมบัติของการเขียนโปรแกรมขั้นสูงที่สนับสนุนในภาษา C++ อย่างเต็มรูปแบบ

ภาษา C++ เป็นภาษาคอมพิวเตอร์เพื่อวัตถุประสงค์ทั่วไป ซึ่งสามารถเขียนโปรแกรมได้ทั้งแบบออบเจ็ค และการเขียนแบบปกติทั่วไป และยังมีเครื่องมืออำนวยความสะดวกในการจัดการและเข้าถึงระดับหน่วยความจำ นอกจากนี้มันยังถูกนำไปใช้ในการเขียนโปรแกรมแบบต่างๆ มากมาย เช่น โปรแกรมคอมพิวเตอร์ ระบบฝังตัว (Embedded) เว็บเซิร์ฟเวอร์ การพัฒนาเกม และแอพพลิเคชันที่ต้องการประสิทธิภาพอย่างสูง

ภาษา C++ เป็นภาษาที่ถูกออกแบบมาในการเขียนโปรแกรมระบบ ซึ่งมีประสิทธิภาพและความยืดหยุ่นในการออกแบบโปรแกรมสูง C++ เป็นภาษาที่ต้องคอมไพล์ก่อนที่จะนำไปใช้งาน ซึ่งสามารถพัฒนาได้ในหลายๆ แพลตฟอร์ม ซึ่งได้รับการสนับสนุนโดยองค์กรต่างๆ ที่ประกอบไปด้วย Free Software Foundation (FSF's GCC) LLVM Microsoft Intel และ IBM
C++ นั้นถูกกำหนดให้เป็นภาษาที่เป็นมาตรฐานโดย International Organization for Standardization (ISO) ซึ่งเวอร์ชันล่าสุดนั้นเผยแพร่ในธันวาคม 2014 คือ ISO/IEC 14882:2014 หรือที่รู้จักกันในชื่อของ C++14 โดยที่ภาษา C++ ได้เริ่มกำหนดมาตราฐานครั้งแรกในปี 1998 คือ ISO/IEC 14882:1998 ภาษา C++ ถูกพัฒนาโดย Bjarne Stroustrup ที่ Bell Labs ตั้งแต่ปี 1979 ซึ่งในตอนแรกเป็นส่วนขยายของภาษา C โดยที่เขาต้องการที่จะพัฒนาภาษาที่มีประสิทธิภาพและยืดหยุ่นเหมือนกับภาษา C และยังมีคุณสมบัติใหม่ที่สูงกว่าสำหรับพัฒนาโปรแกรม

Bjarne Stroustrup นักวิทยาศาสตร์คอมพิวเตอร์ชาวเดนมาร์ก ได้สร้างภาษา C++ ขึ้นในปี 1979 โดยเขาเริ่มจาก "C with Classes" ซึ่งเป็นภาษาก่อนหน้าของภาษา C++ แรงจูงใจสำหรับการสร้างภาษาใหม่นั้นมีต้นกำเนิดมาจากประสบการณ์ในการเขียนโปรแกรมสำหรับงานวิจัยในการศึกษาระดับปริญญาเอกของเขา ในขณะที่ Stroustrup เริ่มต้นการทำงานที่ AT&T Bell Labs เขามีปัญหาในการวิเคราะห์ UNIX kernel ซึ่งเกี่ยวกับ distributed computing จากการจดจำในประสบการณ์ปริญญาเอกของเขา Stroustrup ตั้งใจว่าจะเพิ่มความสามารถให้ภาษา C กับคุณสมบัติที่เหมือนภาษา Simula เขาเลือกภาษา C เพราะว่ามันเป็นภาษาเขียนโปรแกรมเพื่อวัตถุประสงค์ทั่วไป ที่ทำงานเร็ว สะดวกใช้งานง่ายและใช้กันอย่างแพร่หลาย จนกระทั่งในปี 2011 มาตฐานของ C++11 ได้ถูกเผยแพร่ โดยการเพิ่มคุณสมบัติใหม่เข้ามามากมาย รวมทั้งการเพิ่มเติมขนาดของไลบรารี่มาตรฐาน และให้ความสะดวกแก่โปรแกรมเมอร์ภาษา C++ เป็นอย่างมาก

หลังจากบทเรียนนี้เสร็จสิ้น คุณจะเข้าใจและสามารถสร้างแอพพลิเคชันของคุณเอง เพราะว่าภาษา C++ เป็นพื้นฐานที่นำไปสู่การกำเนิดภาษาอื่นๆ และเป็นภาษาที่พัฒนามาจากภาษา C การเริ่มต้นเรียนรู้กับภาษา C++ ยังช่วยให้คุณเข้าใจและเรียนภาษาอื่นได้ง่ายขึ้น เช่น ภาษา C# ภาษา Java หรือ ภาษา PHP เป็นต้น

 JavaScript คือ ภาษาคอมพิวเตอร์สำหรับการเขียนโปรแกรมบนระบบอินเทอร์เน็ต ที่กำลังได้รับความนิยมอย่างสูง Java JavaScript เป็น ภาษาสคริปต์เชิงวัตถุ (ที่เรียกกันว่า "สคริปต์" (script) ซึ่งในการสร้างและพัฒนาเว็บไซต์ (ใช่ร่วมกับ HTML) เพื่อให้เว็บไซต์ของเราดูมีการเคลื่อนไหว สามารถตอบสนองผู้ใช้งานได้มากขึ้น ซึ่งมีวิธีการทำงานในลักษณะ "แปลความและดำเนินงานไปทีละคำสั่ง" (interpret) หรือเรียกว่า อ็อบเจ็กโอเรียลเต็ด (Object Oriented Programming) ที่มีเป้าหมายในการ ออกแบบและพัฒนาโปรแกรมในระบบอินเทอร์เน็ต สำหรับผู้เขียนด้วยภาษา HTML สามารถทำงานข้ามแพลตฟอร์มได้ โดยทำงานร่วมกับ ภาษา HTML และภาษา Java ได้ทั้งทางฝั่งไคลเอนต์ (Client) และ ทางฝั่งเซิร์ฟเวอร์ (Server)
     JavaScript ถูกพัฒนาขึ้นโดย เน็ตสเคปคอมมิวนิเคชันส์ (Netscape Communications Corporation) โดยใช้ชื่อว่า Live Script ออกมาพร้อมกับ Netscape Navigator2.0 เพื่อใช้สร้างเว็บเพจโดยติดต่อกับเซิร์ฟเวอร์แบบ Live Wire ต่อมาเน็ตสเคปจึงได้ร่วมมือกับ บริษัทซันไมโครซิสเต็มส์ปรับปรุงระบบของบราวเซอร์เพื่อให้สามารถติดต่อใช้งานกับภาษาจาวาได้ และได้ปรับปรุง LiveScript ใหม่เมื่อ ปี 2538 แล้วตั้งชื่อใหม่ว่า JavaScript JavaScript สามารถทำให้ การสร้างเว็บเพจ มีลูกเล่น ต่าง ๆ มากมาย และยังสามารถโต้ตอบกับผู้ใช้ได้อย่างทันที เช่น การใช้เมาส์คลิก หรือ การกรอกข้อความในฟอร์ม เป็นต้น
     เนื่องจาก JavaScript ช่วยให้ผู้พัฒนา สามารถสร้างเว็บเพจได้ตรงกับความต้องการ และมีความน่าสนใจมากขึ้น ประกอบกับเป็นภาษาเปิด ที่ใครก็สามารถนำไปใช้ได้ ดังนั้นจึงได้รับความนิยมเป็นอย่างสูง มีการใช้งานอย่างกว้างขวาง รวมทั้งได้ถูกกำหนดให้เป็นมาตรฐานโดย ECMA การทำงานของ JavaScript จะต้องมีการแปลความคำสั่ง ซึ่งขั้นตอนนี้จะถูกจัดการโดยบราวเซอร์ (เรียกว่าเป็น client-side script) ดังนั้น JavaScript จึงสามารถทำงานได้ เฉพาะบนบราวเซอร์ที่สนับสนุน ซึ่งปัจจุบันบราวเซอร์เกือบทั้งหมดก็สนับสนุน JavaScript แล้ว อย่างไรก็ดี สิ่งที่ต้องระวังคือ JavaScript มีการพัฒนาเป็นเวอร์ชั่นใหม่ๆออกมาด้วย (ปัจจุบันคือรุ่น 1.5) ดังนั้น ถ้านำโค้ดของเวอร์ชั่นใหม่ ไปรันบนบราวเซอร์รุ่นเก่าที่ยังไม่สนับสนุน ก็อาจจะทำให้เกิด error ได้

JavaScript ทำอะไรได้บ้าง
    1.JavaScript ทำให้สามารถใช้เขียนโปรแกรมแบบง่ายๆได้ โดยไม่ต้องพึ่งภาษาอื่น
    2.JavaScript มีคำสั่งที่ตอบสนองกับผู้ใช้งาน เช่นเมื่อผู้ใช้คลิกที่ปุ่ม หรือ Checkbox ก็สามารถสั่งให้เปิดหน้าใหม่ได้ ทำให้เว็บไซต์ของเรามีปฏิสัมพันธ์กับผู้ใช้งานมากขึ้น นี่คือข้อดีของ JavaScript เลยก็ว่าได้ที่ทำให้เว็บไซต์ดังๆทั้งหลายเช่น Google Map ต่างหันมาใช้
    3.JavaScript สามารถเขียนหรือเปลี่ยนแปลง HTML Element ได้ นั่นคือสามารถเปลี่ยนแปลงรูปแบบการแสดงผลของเว็บไซต์ได้ หรือหน้าแสดงเนื้อหาสามารถซ่อนหรือแสดงเนื้อหาได้แบบง่ายๆนั่นเอง
    4.JavaScript สามารถใช้ตรวจสอบข้อมูลได้ สังเกตว่าเมื่อเรากรอกข้อมูลบางเว็บไซต์ เช่น Email เมื่อเรากรอกข้อมูลผิดจะมีหน้าต่างฟ้องขึ้นมาว่าเรากรอกผิด หรือลืมกรอกอะไรบางอย่าง เป็นต้น
    5.JavaScript สามารถใช้ในการตรวจสอบผู้ใช้ได้เช่น ตรวจสอบว่าผู้ใช้ ใช้ web browser อะไร
    6.JavaScript สร้าง Cookies (เก็บข้อมูลของผู้ใช้ในคอมพิวเตอร์ของผู้ใช้เอง) ได้

ข้อดีและข้อเสียของ Java JavaScript
     การทำงานของ JavaScript เกิดขึ้นบนบราวเซอร์ (เรียกว่าเป็น client-side script) ดังนั้นไม่ว่าคุณจะใช้เซิร์ฟเวอร์อะไร หรือที่ไหน ก็ยังคงสามารถใช้ JavaScript ในเว็บเพจได้ ต่างกับภาษาสคริปต์อื่น เช่น Perl, PHP หรือ ASP ซึ่งต้องแปลความและทำงานที่ตัวเครื่องเซิร์ฟเวอร์ (เรียกว่า server-side script) ดังนั้นจึงต้องใช้บนเซิร์ฟเวอร์ ที่สนับสนุนภาษาเหล่านี้เท่านั้น อย่างไรก็ดี จากลักษณะดังกล่าวก็ทำให้ JavaScript มีข้อจำกัด คือไม่สามารถรับและส่งข้อมูลต่างๆ กับเซิร์ฟเวอร์โดยตรง เช่น การอ่านไฟล์จากเซิร์ฟเวอร์ เพื่อนำมาแสดงบนเว็บเพจ หรือรับข้อมูลจากผู้ชม เพื่อนำไปเก็บบนเซิร์ฟเวอร์ เป็นต้น ดังนั้นงานลักษณะนี้ จึงยังคงต้องอาศัยภาษา server-side script อยู่ (ความจริง JavaScript ที่ทำงานบนเซิร์ฟเวอร์เวอร์ก็มี ซึ่งต้องอาศัยเซิร์ฟเวอร์ที่สนับสนุนโดยเฉพาะเช่นกัน แต่ไม่เป็นที่นิยมนัก)
     
     Cframe มอน
       local placeId = game.PlaceId
  Magnet = true
  if placeId == 2753915549 then
	 OldWorld = true
  elseif placeId == 4442272183 then
	 NewWorld = true
 elseif placeId == 7449423635 then
	Third = true
  end
  function Click()
	 game:GetService'VirtualUser':CaptureController()
	 game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
  end
  function CheckQuest()
	 local MyLevel = game.Players.LocalPlayer.Data.Level.Value
	 if OldWorld then
		if MyLevel == 1 or MyLevel <= 9 then -- Bandit
			  Ms = "Bandit [Lv. 5]"
			  NaemQuest = "BanditQuest1"
			  LevelQuest = 1
			  NameMon = "Bandit"
			  CFrameQuest = CFrame.new(1061.66699, 16.5166187, 1544.52905, -0.942978859, -3.33851502e-09, 0.332852632, 7.04340497e-09, 1, 2.99841325e-08, -0.332852632, 3.06188177e-08, -0.942978859)
			  CFrameMon = CFrame.new(1199.31287, 52.2717781, 1536.91516, -0.929782331, 6.60215846e-08, -0.368109822, 3.9077392e-08, 1, 8.06501603e-08, 0.368109822, 6.06023249e-08, -0.929782331)
		elseif MyLevel == 10 or MyLevel <= 14 then -- Monkey
			  Ms = "Monkey [Lv. 14]"
			  NaemQuest = "JungleQuest"
			  LevelQuest = 1
			  NameMon = "Monkey"
			  CFrameQuest = CFrame.new(-1604.12012, 36.8521118, 154.23732, 0.0648873374, -4.70858913e-06, -0.997892559, 1.41431883e-07, 1, -4.70933674e-06, 0.997892559, 1.64442184e-07, 0.0648873374)
			  CFrameMon = CFrame.new(-1402.74609, 98.5633316, 90.6417007, 0.836947978, 0, 0.547282517, -0, 1, -0, -0.547282517, 0, 0.836947978)
		elseif MyLevel == 15 or MyLevel <= 29 then -- Gorilla
			  Ms = "Gorilla [Lv. 20]"
			  NaemQuest = "JungleQuest"
			  LevelQuest = 2
			  NameMon = "Gorilla"
			  CFrameQuest = CFrame.new(-1604.12012, 36.8521118, 154.23732, 0.0648873374, -4.70858913e-06, -0.997892559, 1.41431883e-07, 1, -4.70933674e-06, 0.997892559, 1.64442184e-07, 0.0648873374)
			  CFrameMon = CFrame.new(-1223.52808, 6.27936459, -502.292664, 0.310949147, -5.66602516e-08, 0.950426519, -3.37275488e-08, 1, 7.06501808e-08, -0.950426519, -5.40241736e-08, 0.310949147)
		elseif MyLevel == 30 or MyLevel <= 39 then -- Pirate
			  Ms = "Pirate [Lv. 35]"
			  NaemQuest = "BuggyQuest1"
			  LevelQuest = 1
			  NameMon = "Pirate"
			  CFrameQuest = CFrame.new(-1139.59717, 4.75205183, 3825.16211, -0.959730506, -7.5857054e-09, 0.280922383, -4.06310328e-08, 1, -1.11807175e-07, -0.280922383, -1.18718916e-07, -0.959730506)
			  CFrameMon = CFrame.new(-1219.32324, 4.75205183, 3915.63452, -0.966492832, -6.91238853e-08, 0.25669381, -5.21195496e-08, 1, 7.3047012e-08, -0.25669381, 5.72206496e-08, -0.966492832)
		elseif MyLevel == 40 or MyLevel <= 59 then -- Brute
			  Ms = "Brute [Lv. 45]"
			  NaemQuest = "BuggyQuest1"
			  LevelQuest = 2
			  NameMon = "Brute"
			  CFrameQuest = CFrame.new(-1139.59717, 4.75205183, 3825.16211, -0.959730506, -7.5857054e-09, 0.280922383, -4.06310328e-08, 1, -1.11807175e-07, -0.280922383, -1.18718916e-07, -0.959730506)
			  CFrameMon = CFrame.new(-1146.49646, 96.0936813, 4312.1333, -0.978175163, -1.53222057e-08, 0.207781896, -3.33316912e-08, 1, -8.31738873e-08, -0.207781896, -8.82843523e-08, -0.978175163)
		elseif MyLevel == 60 or MyLevel <= 74 then -- Desert Bandit
			  Ms = "Desert Bandit [Lv. 60]"
			  NaemQuest = "DesertQuest"
			  LevelQuest = 1
			  NameMon = "Desert Bandit"
			  CFrameQuest = CFrame.new(897.031128, 6.43846416, 4388.97168, -0.804044724, 3.68233266e-08, 0.594568789, 6.97835176e-08, 1, 3.24365246e-08, -0.594568789, 6.75715199e-08, -0.804044724)
			  CFrameMon = CFrame.new(932.788818, 6.4503746, 4488.24609, -0.998625934, 3.08948351e-08, 0.0524050146, 2.79967303e-08, 1, -5.60361286e-08, -0.0524050146, -5.44919629e-08, -0.998625934)
		elseif MyLevel == 75 or MyLevel <= 89 then -- Desert Officre
			  Ms = "Desert Officer [Lv. 70]"
			  NaemQuest = "DesertQuest"
			  LevelQuest = 2
			  NameMon = "Desert Officer"
			  CFrameQuest = CFrame.new(897.031128, 6.43846416, 4388.97168, -0.804044724, 3.68233266e-08, 0.594568789, 6.97835176e-08, 1, 3.24365246e-08, -0.594568789, 6.75715199e-08, -0.804044724)
			  CFrameMon = CFrame.new(1580.03198, 4.61375761, 4366.86426, 0.135744005, -6.44280718e-08, -0.990743816, 4.35738308e-08, 1, -5.90598574e-08, 0.990743816, -3.51534837e-08, 0.135744005)
		elseif MyLevel == 90 or MyLevel <= 99 then -- Snow Bandits
			  Ms = "Snow Bandit [Lv. 90]"
			  NaemQuest = "SnowQuest"
			  LevelQuest = 1
			  NameMon = "Snow Bandits"
			  CFrameQuest = CFrame.new(1384.14001, 87.272789, -1297.06482, 0.348555952, -2.53947841e-09, -0.937287986, 1.49860568e-08, 1, 2.86358204e-09, 0.937287986, -1.50443711e-08, 0.348555952)
			  CFrameMon = CFrame.new(1370.24316, 102.403511, -1411.52905, 0.980274439, -1.12995728e-08, 0.197641045, -9.57343449e-09, 1, 1.04655214e-07, -0.197641045, -1.04482936e-07, 0.980274439)
		elseif MyLevel == 100 or MyLevel <= 119 then -- Snowman
			  Ms = "Snowman [Lv. 100]"
			  NaemQuest = "SnowQuest"
			  LevelQuest = 2
			  NameMon = "Snowman"
			  CFrameQuest = CFrame.new(1384.14001, 87.272789, -1297.06482, 0.348555952, -2.53947841e-09, -0.937287986, 1.49860568e-08, 1, 2.86358204e-09, 0.937287986, -1.50443711e-08, 0.348555952)
			  CFrameMon = CFrame.new(1370.24316, 102.403511, -1411.52905, 0.980274439, -1.12995728e-08, 0.197641045, -9.57343449e-09, 1, 1.04655214e-07, -0.197641045, -1.04482936e-07, 0.980274439)
		elseif MyLevel == 120 or MyLevel <= 149 then -- Chief Petty Officer
			  Ms = "Chief Petty Officer [Lv. 120]"
			  NaemQuest = "MarineQuest2"
			  LevelQuest = 1
			  NameMon = "Chief Petty Officer"
			  CFrameQuest = CFrame.new(-5035.0835, 28.6520386, 4325.29443, 0.0243340395, -7.08064647e-08, 0.999703884, -6.36926814e-08, 1, 7.23777944e-08, -0.999703884, -6.54350671e-08, 0.0243340395)
			  CFrameMon = CFrame.new(-4882.8623, 22.6520386, 4255.53516, 0.273695946, -5.40380647e-08, -0.96181643, 4.37720793e-08, 1, -4.37274998e-08, 0.96181643, -3.01326679e-08, 0.273695946)
		elseif MyLevel == 150 or MyLevel <= 174 then -- Sky Bandit
			  Ms = "Sky Bandit [Lv. 150]"
			  NaemQuest = "SkyQuest"
			  LevelQuest = 1
			  NameMon = "Sky Bandit"
			  CFrameQuest = CFrame.new(-4841.83447, 717.669617, -2623.96436, -0.875942111, 5.59710216e-08, -0.482416272, 3.04023082e-08, 1, 6.08195947e-08, 0.482416272, 3.86078725e-08, -0.875942111)
			  CFrameMon = CFrame.new(-4970.74219, 294.544342, -2890.11353, -0.994874597, -8.61311236e-08, -0.101116329, -9.10836206e-08, 1, 4.43614923e-08, 0.101116329, 5.33441664e-08, -0.994874597)
		elseif MyLevel == 175 or MyLevel <= 224 then -- Dark Master
			  Ms = "Dark Master [Lv. 175]"
			  NaemQuest = "SkyQuest"
			  LevelQuest = 2
			  NameMon = "Dark Master"
			  CFrameQuest = CFrame.new(-4841.83447, 717.669617, -2623.96436, -0.875942111, 5.59710216e-08, -0.482416272, 3.04023082e-08, 1, 6.08195947e-08, 0.482416272, 3.86078725e-08, -0.875942111)
			  CFrameMon = CFrame.new(-5220.58594, 430.693298, -2278.17456, -0.925375521, 1.12086873e-08, 0.379051805, -1.05115507e-08, 1, -5.52320891e-08, -0.379051805, -5.50948407e-08, -0.925375521)
		elseif MyLevel == 225 or MyLevel <= 274 then -- Toga Warrior
			  Ms = "Toga Warrior [Lv. 225]"
			  NaemQuest = "ColosseumQuest"
			  LevelQuest = 1
			  NameMon = "Toga Warrior"
			  CFrameQuest = CFrame.new(-1576.11743, 7.38933945, -2983.30762, 0.576966345, 1.22114863e-09, 0.816767931, -3.58496594e-10, 1, -1.24185606e-09, -0.816767931, 4.2370063e-10, 0.576966345)
			  CFrameMon = CFrame.new(-1779.97583, 44.6077499, -2736.35474, 0.984437346, 4.10396339e-08, 0.175734788, -3.62286876e-08, 1, -3.05844168e-08, -0.175734788, 2.3741821e-08, 0.984437346)
		elseif MyLevel == 275 or MyLevel <= 299 then -- Gladiato
			  Ms = "Gladiator [Lv. 275]"
			  NaemQuest = "ColosseumQuest"
			  LevelQuest = 2
			  NameMon = "Gladiato"
			  CFrameQuest = CFrame.new(-1576.11743, 7.38933945, -2983.30762, 0.576966345, 1.22114863e-09, 0.816767931, -3.58496594e-10, 1, -1.24185606e-09, -0.816767931, 4.2370063e-10, 0.576966345)
			  CFrameMon = CFrame.new(-1274.75903, 58.1895943, -3188.16309, 0.464524001, 6.21005611e-08, 0.885560572, -4.80449414e-09, 1, -6.76054768e-08, -0.885560572, 2.71497012e-08, 0.464524001)
		elseif MyLevel == 300 or MyLevel <= 329 then -- Military Soldier
			  Ms = "Military Soldier [Lv. 300]"
			  NaemQuest = "MagmaQuest"
			  LevelQuest = 1
			  NameMon = "Military Soldier"
			  CFrameQuest = CFrame.new(-5316.55859, 12.2370615, 8517.2998, 0.588437557, -1.37880001e-08, -0.808542669, -2.10116209e-08, 1, -3.23446478e-08, 0.808542669, 3.60215964e-08, 0.588437557)
			  CFrameMon = CFrame.new(-5363.01123, 41.5056877, 8548.47266, -0.578253984, -3.29503091e-10, 0.815856814, 9.11209668e-08, 1, 6.498761e-08, -0.815856814, 1.11920997e-07, -0.578253984)
		elseif MyLevel == 300 or MyLevel <= 374 then -- Military Spy
			  Ms = "Military Spy [Lv. 330]"
			  NaemQuest = "MagmaQuest"
			  LevelQuest = 2
			  NameMon = "Military Spy"
			  CFrameQuest = CFrame.new(-5316.55859, 12.2370615, 8517.2998, 0.588437557, -1.37880001e-08, -0.808542669, -2.10116209e-08, 1, -3.23446478e-08, 0.808542669, 3.60215964e-08, 0.588437557)
			  CFrameMon = CFrame.new(-5787.99023, 120.864456, 8762.25293, -0.188358366, -1.84706277e-08, 0.982100308, -1.23782129e-07, 1, -4.93306951e-09, -0.982100308, -1.22495649e-07, -0.188358366)
		elseif MyLevel == 375 or MyLevel <= 399 then -- Fishman Warrior
			  Ms = "Fishman Warrior [Lv. 375]"
			  NaemQuest = "FishmanQuest"
			  LevelQuest = 1
			  NameMon = "Fishman Warrior"
			  CFrameQuest = CFrame.new(61122.5625, 18.4716396, 1568.16504, 0.893533468, 3.95251609e-09, 0.448996574, -2.34327455e-08, 1, 3.78297464e-08, -0.448996574, -4.43233645e-08, 0.893533468)
			  CFrameMon = CFrame.new(60946.6094, 48.6735229, 1525.91687, -0.0817126185, 8.90751153e-08, 0.996655822, 2.00889794e-08, 1, -8.77269599e-08, -0.996655822, 1.28533992e-08, -0.0817126185)
		elseif MyLevel == 400 or MyLevel <= 449 then -- Fishman Commando
			  Ms = "Fishman Commando [Lv. 400]"
			  NaemQuest = "FishmanQuest"
			  LevelQuest = 2
			  NameMon = "Fishman Commando"
			  CFrameQuest = CFrame.new(61122.5625, 18.4716396, 1568.16504, 0.893533468, 3.95251609e-09, 0.448996574, -2.34327455e-08, 1, 3.78297464e-08, -0.448996574, -4.43233645e-08, 0.893533468)
			  CFrameMon = CFrame.new(61885.5039, 18.4828243, 1504.17896, 0.577502489, 0, -0.816389024, -0, 1.00000012, -0, 0.816389024, 0, 0.577502489)
		elseif MyLevel == 450 or MyLevel <= 474 then -- God's Guards
			  Ms = "God's Guard [Lv. 450]"
			  NaemQuest = "SkyExp1Quest"
			  LevelQuest = 1
			  NameMon = "God's Guards"
			  CFrameQuest = CFrame.new(-4721.71436, 845.277161, -1954.20105, -0.999277651, -5.56969759e-09, 0.0380011722, -4.14751478e-09, 1, 3.75035256e-08, -0.0380011722, 3.73188307e-08, -0.999277651)
			  CFrameMon = CFrame.new(-4716.95703, 853.089722, -1933.92542, -0.93441087, -6.77488776e-09, -0.356197298, 1.12145182e-08, 1, -4.84390199e-08, 0.356197298, -4.92565206e-08, -0.93441087)
		elseif MyLevel == 475 or MyLevel <= 524 then -- Shandas
			  Ms = "Shanda [Lv. 475]"
			  NaemQuest = "SkyExp1Quest"
			  LevelQuest = 2
			  NameMon = "Shandas"
			  CFrameQuest = CFrame.new(-7863.63672, 5545.49316, -379.826324, 0.362120807, -1.98046344e-08, -0.93213129, 4.05822291e-08, 1, -5.48095125e-09, 0.93213129, -3.58431969e-08, 0.362120807)
			  CFrameMon = CFrame.new(-7685.12354, 5601.05127, -443.171509, 0.150056243, 1.79768236e-08, -0.988677442, 6.67798661e-09, 1, 1.91962481e-08, 0.988677442, -9.48289181e-09, 0.150056243)
		elseif MyLevel == 525 or MyLevel <= 549 then -- Royal Squad
			  Ms = "Royal Squad [Lv. 525]"
			  NaemQuest = "SkyExp2Quest"
			  LevelQuest = 1
			  NameMon = "Royal Squad"
			  CFrameQuest = CFrame.new(-7902.66895, 5635.96387, -1411.71802, 0.0504222959, 2.5710392e-08, 0.998727977, 1.12541557e-07, 1, -3.14249675e-08, -0.998727977, 1.13982921e-07, 0.0504222959)
			  CFrameMon = CFrame.new(-7685.02051, 5606.87842, -1442.729, 0.561947823, 7.69527464e-09, -0.827172697, -4.24974544e-09, 1, 6.41599973e-09, 0.827172697, -9.01838604e-11, 0.561947823)
		elseif MyLevel == 550 or MyLevel <= 624 then -- Royal Soldier
			  Ms = "Royal Soldier [Lv. 550]"
			  NaemQuest = "SkyExp2Quest"
			  LevelQuest = 2
			  NameMon = "Royal Soldier"
			  CFrameQuest = CFrame.new(-7902.66895, 5635.96387, -1411.71802, 0.0504222959, 2.5710392e-08, 0.998727977, 1.12541557e-07, 1, -3.14249675e-08, -0.998727977, 1.13982921e-07, 0.0504222959)
			  CFrameMon = CFrame.new(-7864.44775, 5661.94092, -1708.22351, 0.998389959, 2.28686137e-09, -0.0567218624, 1.99431383e-09, 1, 7.54200258e-08, 0.0567218624, -7.54117195e-08, 0.998389959)
		elseif MyLevel == 625 or MyLevel <= 649 then -- Galley Pirate
			  Ms = "Galley Pirate [Lv. 625]"
			  NaemQuest = "FountainQuest"
			  LevelQuest = 1
			  NameMon = "Galley Pirate"
			  CFrameQuest = CFrame.new(5254.60156, 38.5011406, 4049.69678, -0.0504891425, -3.62066501e-08, -0.998724639, -9.87921389e-09, 1, -3.57534553e-08, 0.998724639, 8.06145284e-09, -0.0504891425)
			  CFrameMon = CFrame.new(5595.06982, 41.5013695, 3961.47095, -0.992138803, -2.11610267e-08, -0.125142589, -1.34249509e-08, 1, -6.26613996e-08, 0.125142589, -6.04887518e-08, -0.992138803)
		elseif MyLevel >= 650 then -- Galley Captain
			  Ms = "Galley Captain [Lv. 650]"
			  NaemQuest = "FountainQuest"
			  LevelQuest = 2
			  NameMon = "Galley Captain"
			  CFrameQuest = CFrame.new(5254.60156, 38.5011406, 4049.69678, -0.0504891425, -3.62066501e-08, -0.998724639, -9.87921389e-09, 1, -3.57534553e-08, 0.998724639, 8.06145284e-09, -0.0504891425)
			  CFrameMon = CFrame.new(5658.5752, 38.5361786, 4928.93506, -0.996873081, 2.12391046e-06, -0.0790185928, 2.16989656e-06, 1, -4.96097414e-07, 0.0790185928, -6.66008248e-07, -0.996873081)
		end
	 end
	 if NewWorld then
		if MyLevel == 700 or MyLevel <= 724 then -- Raider [Lv. 700]
			  Ms = "Raider [Lv. 700]"
			  NaemQuest = "Area1Quest"
			  LevelQuest = 1
			  NameMon = "Raider"
			  CFrameQuest = CFrame.new(-424.080078, 73.0055847, 1836.91589, 0.253544956, -1.42165932e-08, 0.967323601, -6.00147771e-08, 1, 3.04272909e-08, -0.967323601, -6.5768397e-08, 0.253544956)
			  CFrameMon = CFrame.new(-737.026123, 39.1748352, 2392.57959, 0.272128761, 0, -0.962260842, -0, 1, -0, 0.962260842, 0, 0.272128761)
		elseif MyLevel == 725 or MyLevel <= 774 then -- Mercenary [Lv. 725]
			  Ms = "Mercenary [Lv. 725]"
			  NaemQuest = "Area1Quest"
			  LevelQuest = 2
			  NameMon = "Mercenary"
			  CFrameQuest = CFrame.new(-424.080078, 73.0055847, 1836.91589, 0.253544956, -1.42165932e-08, 0.967323601, -6.00147771e-08, 1, 3.04272909e-08, -0.967323601, -6.5768397e-08, 0.253544956)
			  CFrameMon = CFrame.new(-973.731995, 95.8733215, 1836.46936, 0.999135971, 2.02326991e-08, -0.0415605344, -1.90767793e-08, 1, 2.82094952e-08, 0.0415605344, -2.73922804e-08, 0.999135971)
		elseif MyLevel == 775 or MyLevel <= 799 then -- Swan Pirate [Lv. 775]
			  Ms = "Swan Pirate [Lv. 775]"
			  NaemQuest = "Area2Quest"
			  LevelQuest = 1
			  NameMon = "Swan Pirate"
			  CFrameQuest = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771, 1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)
			  CFrameMon = CFrame.new(970.369446, 142.653198, 1217.3667, 0.162079468, -4.85452638e-08, -0.986777723, 1.03357589e-08, 1, -4.74980872e-08, 0.986777723, -2.50063148e-09, 0.162079468)
		elseif MyLevel == 800 or MyLevel <= 874 then -- Factory Staff [Lv. 800]
			  Ms = "Factory Staff [Lv. 800]"
			  NaemQuest = "Area2Quest"
			  LevelQuest = 2
			  NameMon = "Factory Staff"
			  CFrameQuest = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771, 1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)
			  CFrameMon = CFrame.new(296.786499, 72.9948196, -57.1298141, -0.876037002, -5.32364979e-08, 0.482243896, -3.87658332e-08, 1, 3.99718729e-08, -0.482243896, 1.63222538e-08, -0.876037002)
		elseif MyLevel == 875 or MyLevel <= 899 then -- Marine Lieutenant [Lv. 875]
			  Ms = "Marine Lieutenant [Lv. 875]"
			  NaemQuest = "MarineQuest3"
			  LevelQuest = 1
			  NameMon = "Marine Lieutenant"
			  CFrameQuest = CFrame.new(-2442.65015, 73.0511475, -3219.11523, -0.873540044, 4.2329841e-08, -0.486752301, 5.64383384e-08, 1, -1.43220786e-08, 0.486752301, -3.99823996e-08, -0.873540044)
			  CFrameMon = CFrame.new(-2913.26367, 73.0011826, -2971.64282, 0.910507619, 0, 0.413492233, 0, 1.00000012, 0, -0.413492233, 0, 0.910507619)
		elseif MyLevel == 900 or MyLevel <= 949 then -- Marine Captain [Lv. 900]
			  Ms = "Marine Captain [Lv. 900]"
			  NaemQuest = "MarineQuest3"
			  LevelQuest = 2
			  NameMon = "Marine Captain"
			  CFrameQuest = CFrame.new(-2442.65015, 73.0511475, -3219.11523, -0.873540044, 4.2329841e-08, -0.486752301, 5.64383384e-08, 1, -1.43220786e-08, 0.486752301, -3.99823996e-08, -0.873540044)
			  CFrameMon = CFrame.new(-1868.67688, 73.0011826, -3321.66333, -0.971402287, 1.06502087e-08, 0.237439692, 3.68856199e-08, 1, 1.06050372e-07, -0.237439692, 1.11775684e-07, -0.971402287)
		elseif MyLevel == 950 or MyLevel <= 974 then -- Zombie [Lv. 950]
			  Ms = "Zombie [Lv. 950]"
			  NaemQuest = "ZombieQuest"
			  LevelQuest = 1
			  NameMon = "Zombie"
			  CFrameQuest = CFrame.new(-5492.79395, 48.5151672, -793.710571, 0.321800292, -6.24695815e-08, 0.946807742, 4.05616092e-08, 1, 5.21931227e-08, -0.946807742, 2.16082796e-08, 0.321800292)
			  CFrameMon = CFrame.new(-5634.83838, 126.067039, -697.665039, -0.992770672, 6.77618939e-09, 0.120025545, 1.65461245e-08, 1, 8.04023372e-08, -0.120025545, 8.18070234e-08, -0.992770672)
		elseif MyLevel == 975 or MyLevel <= 999 then -- Vampire [Lv. 975]
			  Ms = "Vampire [Lv. 975]"
			  NaemQuest = "ZombieQuest"
			  LevelQuest = 2
			  NameMon = "Vampire"
			  CFrameQuest = CFrame.new(-5492.79395, 48.5151672, -793.710571, 0.321800292, -6.24695815e-08, 0.946807742, 4.05616092e-08, 1, 5.21931227e-08, -0.946807742, 2.16082796e-08, 0.321800292)
			  CFrameMon = CFrame.new(-6030.32031, 6.4377408, -1313.5564, -0.856965423, 3.9138893e-08, -0.515373945, -1.12178942e-08, 1, 9.45958547e-08, 0.515373945, 8.68467822e-08, -0.856965423)
		elseif MyLevel == 1000 or MyLevel <= 1049 then -- Snow Trooper [Lv. 1000] **
			  Ms = "Snow Trooper [Lv. 1000]"
			  NaemQuest = "SnowMountainQuest"
			  LevelQuest = 1
			  NameMon = "Snow Trooper"
			  CFrameQuest = CFrame.new(604.964966, 401.457062, -5371.69287, 0.353063971, 1.89520435e-08, -0.935599446, -5.81846002e-08, 1, -1.70033754e-09, 0.935599446, 5.50377841e-08, 0.353063971)
			  CFrameMon = CFrame.new(535.893433, 401.457062, -5329.6958, -0.999524176, 0, 0.0308452044, 0, 1, -0, -0.0308452044, 0, -0.999524176)
		elseif MyLevel == 1050 or MyLevel <= 1099 then -- Winter Warrior [Lv. 1050]
			  Ms = "Winter Warrior [Lv. 1050]"
			  NaemQuest = "SnowMountainQuest"
			  LevelQuest = 2
			  NameMon = "Winter Warrior"
			  CFrameQuest = CFrame.new(604.964966, 401.457062, -5371.69287, 0.353063971, 1.89520435e-08, -0.935599446, -5.81846002e-08, 1, -1.70033754e-09, 0.935599446, 5.50377841e-08, 0.353063971)
			  CFrameMon = CFrame.new(1223.7417, 454.575226, -5170.02148, 0.473996818, 2.56845354e-08, 0.880526543, -5.62456428e-08, 1, 1.10811016e-09, -0.880526543, -5.00510211e-08, 0.473996818)
		elseif MyLevel == 1100 or MyLevel <= 1124 then -- Lab Subordinate [Lv. 1100]
			  Ms = "Lab Subordinate [Lv. 1100]"
			  NaemQuest = "IceSideQuest"
			  LevelQuest = 1
			  NameMon = "Lab Subordinate"
			  CFrameQuest = CFrame.new(-6060.10693, 15.9868021, -4904.7876, -0.411000341, -5.06538868e-07, 0.91163528, 1.26306062e-07, 1, 6.12581289e-07, -0.91163528, 3.66916197e-07, -0.411000341)
			  CFrameMon = CFrame.new(-5769.2041, 37.9288292, -4468.38721, -0.569419742, -2.49055017e-08, 0.822046936, -6.96206541e-08, 1, -1.79282633e-08, -0.822046936, -6.74401548e-08, -0.569419742)
		elseif MyLevel == 1125 or MyLevel <= 1174 then -- Horned Warrior [Lv. 1125]
			  Ms = "Horned Warrior [Lv. 1125]"
			  NaemQuest = "IceSideQuest"
			  LevelQuest = 2
			  NameMon = "Horned Warrior"
			  CFrameQuest = CFrame.new(-6060.10693, 15.9868021, -4904.7876, -0.411000341, -5.06538868e-07, 0.91163528, 1.26306062e-07, 1, 6.12581289e-07, -0.91163528, 3.66916197e-07, -0.411000341)
			  CFrameMon = CFrame.new(-6400.85889, 24.7645149, -5818.63574, -0.964845479, 8.65926566e-08, -0.262817472, 3.98261392e-07, 1, -1.13260398e-06, 0.262817472, -1.19745812e-06, -0.964845479)
		elseif MyLevel == 1175 or MyLevel <= 1199 then -- Magma Ninja [Lv. 1175]
			  Ms = "Magma Ninja [Lv. 1175]"
			  NaemQuest = "FireSideQuest"
			  LevelQuest = 1
			  NameMon = "Magma Ninja"
			  CFrameQuest = CFrame.new(-5431.09473, 15.9868021, -5296.53223, 0.831796765, 1.15322464e-07, -0.555080295, -1.10814341e-07, 1, 4.17010995e-08, 0.555080295, 2.68240168e-08, 0.831796765)
			  CFrameMon = CFrame.new(-5496.65576, 58.6890411, -5929.76855, -0.885073781, 0, -0.465450764, 0, 1.00000012, -0, 0.465450764, 0, -0.885073781)
		elseif MyLevel == 1200 or MyLevel <= 1249 then -- Lava Pirate [Lv. 1200]
			  Ms = "Lava Pirate [Lv. 1200]"
			  NaemQuest = "FireSideQuest"
			  LevelQuest = 2
			  NameMon = "Lava Pirate"
			  CFrameQuest = CFrame.new(-5431.09473, 15.9868021, -5296.53223, 0.831796765, 1.15322464e-07, -0.555080295, -1.10814341e-07, 1, 4.17010995e-08, 0.555080295, 2.68240168e-08, 0.831796765)
			  CFrameMon = CFrame.new(-5169.71729, 34.1234779, -4669.73633, -0.196780294, 0, 0.98044765, 0, 1.00000012, -0, -0.98044765, 0, -0.196780294)
		elseif MyLevel == 1250 or MyLevel <= 1274 then -- Ship Deckhand [Lv. 1250]
			  Ms = "Ship Deckhand [Lv. 1250]"
			  NaemQuest = "ShipQuest1"
			  LevelQuest = 1
			  NameMon = "Ship Deckhand"
			  CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016, -0.244533166, -0, -0.969640911, -0, 1.00000012, -0, 0.96964103, 0, -0.244533136)
			  CFrameMon = CFrame.new(1163.80872, 138.288452, 33058.4258, -0.998580813, 5.49076979e-08, -0.0532564968, 5.57436763e-08, 1, -1.42118655e-08, 0.0532564968, -1.71604082e-08, -0.998580813)
		elseif MyLevel == 1275 or MyLevel <= 1299 then -- Ship Engineer [Lv. 1275]
			  Ms = "Ship Engineer [Lv. 1275]"
			  NaemQuest = "ShipQuest1"
			  LevelQuest = 2
			  NameMon = "Ship Engineer"
			  CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016, -0.244533166, -0, -0.969640911, -0, 1.00000012, -0, 0.96964103, 0, -0.244533136)
			  CFrameMon = CFrame.new(916.666504, 44.0920448, 32917.207, -0.99746871, -4.85034697e-08, -0.0711069331, -4.8925461e-08, 1, 4.19294288e-09, 0.0711069331, 7.66126895e-09, -0.99746871)
		elseif MyLevel == 1300 or MyLevel <= 1324 then -- Ship Steward [Lv. 1300]
			  Ms = "Ship Steward [Lv. 1300]"
			  NaemQuest = "ShipQuest2"
			  LevelQuest = 1
			  NameMon = "Ship Steward"
			  CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125, -0.869560242, 1.51905191e-08, -0.493826836, 1.44108379e-08, 1, 5.38534195e-09, 0.493826836, -2.43357912e-09, -0.869560242)
			  CFrameMon = CFrame.new(918.743286, 129.591064, 33443.4609, -0.999792814, -1.7070947e-07, -0.020350717, -1.72559169e-07, 1, 8.91351277e-08, 0.020350717, 9.2628369e-08, -0.999792814)
		elseif MyLevel == 1325 or MyLevel <= 1349 then -- Ship Officer [Lv. 1325]
		   Ms = "Ship Officer [Lv. 1325]"
		   NaemQuest = "ShipQuest2"
		   LevelQuest = 2
		   NameMon = "Ship Officer"
		   CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125, -0.869560242, 1.51905191e-08, -0.493826836, 1.44108379e-08, 1, 5.38534195e-09, 0.493826836, -2.43357912e-09, -0.869560242)
		   CFrameMon = CFrame.new(786.051941, 181.474106, 33303.2969, 0.999285698, -5.32193063e-08, 0.0377905183, 5.68968588e-08, 1, -9.62386864e-08, -0.0377905183, 9.83201005e-08, 0.999285698)
		elseif MyLevel == 1350 or MyLevel <= 1374 then -- Arctic Warrior [Lv. 1350]
		   Ms = "Arctic Warrior [Lv. 1350]"
		   NaemQuest = "FrostQuest"
		   LevelQuest = 1
		   NameMon = "Arctic Warrior"
		   CFrameQuest = CFrame.new(5669.43506, 28.2117786, -6482.60107, 0.888092756, 1.02705066e-07, 0.459664226, -6.20391774e-08, 1, -1.03572376e-07, -0.459664226, 6.34646895e-08, 0.888092756)
		   CFrameMon = CFrame.new(5995.07471, 57.3188477, -6183.47314, 0.702747107, -1.53454167e-07, -0.711440146, -1.08168464e-07, 1, -3.22542007e-07, 0.711440146, 3.03620908e-07, 0.702747107)
		elseif MyLevel == 1375 or MyLevel <= 1424 then -- Snow Lurker [Lv. 1375]
		   Ms = "Snow Lurker [Lv. 1375]"
		   NaemQuest = "FrostQuest"
		   LevelQuest = 2
		   NameMon = "Snow Lurker"
		   CFrameQuest = CFrame.new(5669.43506, 28.2117786, -6482.60107, 0.888092756, 1.02705066e-07, 0.459664226, -6.20391774e-08, 1, -1.03572376e-07, -0.459664226, 6.34646895e-08, 0.888092756)
		   CFrameMon = CFrame.new(5518.00684, 60.5559731, -6828.80518, -0.650781393, -3.64292951e-08, 0.759265184, -4.07668654e-09, 1, 4.44854642e-08, -0.759265184, 2.58550248e-08, -0.650781393)
		elseif MyLevel == 1425 or MyLevel <= 1449 then -- Sea Soldier [Lv. 1425]
		   Ms = "Sea Soldier [Lv. 1425]"
		   NaemQuest = "ForgottenQuest"
		   LevelQuest = 1
		   NameMon = "Sea Soldier"
		   CFrameQuest = CFrame.new(-3052.99097, 236.881363, -10148.1943, -0.997911751, 4.42321983e-08, 0.064591676, 4.90968759e-08, 1, 7.37270085e-08, -0.064591676, 7.67442998e-08, -0.997911751)
		   CFrameMon = CFrame.new(-3029.78467, 66.944252, -9777.38184, -0.998552859, 1.09555076e-08, 0.0537791774, 7.79564235e-09, 1, -5.89660658e-08, -0.0537791774, -5.84614881e-08, -0.998552859)
		elseif MyLevel >= 1450 then -- Water Fighter [Lv. 1450]
		   Ms = "Water Fighter [Lv. 1450]"
		   NaemQuest = "ForgottenQuest"
		   LevelQuest = 2
		   NameMon = "Water Fighter"
		   CFrameQuest = CFrame.new(-3052.99097, 236.881363, -10148.1943, -0.997911751, 4.42321983e-08, 0.064591676, 4.90968759e-08, 1, 7.37270085e-08, -0.064591676, 7.67442998e-08, -0.997911751)
		   CFrameMon = CFrame.new(-3262.00098, 298.699615, -10553.6943, -0.233570755, -4.57538185e-08, 0.972339869, -5.80986068e-08, 1, 3.30992194e-08, -0.972339869, -4.87605725e-08, -0.233570755)
		end
	 elseif Third then
		 if MyLevel == 1500 or MyLevel <= 1524 then
			Ms = "Pirate Millionaire [Lv. 1500]"
		   NaemQuest = "PiratePortQuest"
		   LevelQuest = 1
		   NameMon = "Pirate Millionaire"
		   CFrameQuest = CFrame.new(-290.169861, 39.691246, 5581.43408, 0.25875926, 0, 0.965941846, 0, 1, 0, -0.965941846, 0, 0.25875926)
		   CFrameMon = CFrame.new(-350.896179, 35.8283691, 5799.72607, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
		 elseif MyLevel == 1525 or MyLevel <= 1574 then
		Ms = "Pistol Billionaire [Lv. 1525]"
		   NaemQuest = "PiratePortQuest"
		   LevelQuest = 2
		   
		   NameMon = "Pistol Billionaire"
		   CFrameQuest = CFrame.new(-290.169861, 39.691246, 5581.43408, 0.25875926, 0, 0.965941846, 0, 1, 0, -0.965941846, 0, 0.25875926)
		   CFrameMon = CFrame.new(-350.896179, 35.8283691, 5799.72607, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
		 elseif MyLevel == 1575  or MyLevel <= 1599  then
			 Ms = "Dragon Crew Warrior [Lv. 1575]"
		   NaemQuest = "AmazonQuest"
		   LevelQuest = 1
		   NameMon = "Dragon Crew Warrior"
		   CFrameQuest = CFrame.new(5832.79688, 53.2015953, -1101.43604, 0.898790359, -0, -0.438378751, 0, 1, -0, 0.438378751, 0, 0.898790359)
		   CFrameMon = CFrame.new(6130.97705, 36.111084, -1175.04663, -1, 0, 0, 0, 1, 0, 0, 0, -1)  
		 elseif MyLevel == 1600 or MyLevel <= 1624 then
			  Ms = "Dragon Crew Archer [Lv. 1600]"
		   NaemQuest = "AmazonQuest"
		   LevelQuest = 2
		   NameMon = "Dragon Crew Archer"
		   CFrameQuest = CFrame.new(5832.79688, 53.2015953, -1101.43604, 0.898790359, -0, -0.438378751, 0, 1, -0, 0.438378751, 0, 0.898790359)
		   CFrameMon = CFrame.new(6786.99609, 398.514587, 449.414917, 0.681973696, -0, -0.731376648, 0, 1, -0, 0.731376648, 0, 0.681973696)
		 elseif MyLevel == 1625 or MyLevel <= 1649 then
		   Ms = "Female Islander [Lv. 1625]"
		   NaemQuest = "AmazonQuest2"
		   
		   LevelQuest = 1
		   NameMon = "Female Islander"
		   CFrameQuest = CFrame.new(5448.86133, 603.349365, 751.130676, 0, 0, 1, 0, 1, -0, -1, 0, 0)
		   CFrameMon = CFrame.new(4659.69775, 647.820557, 834.697205, 0, 0, -1, 0, 1, 0, 1, 0, 0)
		  elseif MyLevel == 1650 or MyLevel <= 1699 then
		   Ms = "Giant Islander [Lv. 1650]"
		   NaemQuest = "AmazonQuest2"
		   
		   LevelQuest = 2
		   NameMon = "Giant Islander"
					 CFrameQuest = CFrame.new(5448.86133, 603.349365, 751.130676, 0, 0, 1, 0, 1, -0, -1, 0, 0)
		   CFrameMon = CFrame.new(4869.33643, 596.635315, 37.1867523, -0.958187938, 0, -0.286139995, 0, 1, 0, 0.286139995, 0, -0.958187938)
		  elseif MyLevel == 1700 or MyLevel <= 1724 then
			 Ms = "Marine Commodore [Lv. 1700]"
		   NaemQuest = "MarineTreeIsland"
		   
		   LevelQuest = 1
		   NameMon = "Marine Commodore"
		   CFrameQuest = CFrame.new(2180.54126, 30.3531189, -6741.55029, -0.965929747, 0, 0.258804798, 0, 1, 0, -0.258804798, 0, -0.965929747)
		   CFrameMon = CFrame.new(2996.99634, 65.6201782, -7282.29541, 0.173624337, -0, -0.984811902, 0, 1, -0, 0.984811902, 0, 0.173624337) 
		   elseif MyLevel == 1725 or MyLevel <= 1774 then
			 Ms = "Marine Rear Admiral [Lv. 1725]"
		   NaemQuest = "MarineTreeIsland"
		   
		   LevelQuest = 2
		   NameMon = "Marine Rear Admiral"
		   CFrameQuest = CFrame.new(2180.54126, 30.3531189, -6741.55029, -0.965929747, 0, 0.258804798, 0, 1, 0, -0.258804798, 0, -0.965929747)
		   CFrameMon = CFrame.new(3695.38403, 155.158585, -7004.74805, -0.325602531, 0, -0.945506752, 0, 1, 0, 0.945506752, 0, -0.325602531) 
					  elseif MyLevel == 1775 or MyLevel <= 1800 then
			 Ms = "Fishman Raider [Lv. 1775]"
		   NaemQuest = "DeepForestIsland3"
		   
		   LevelQuest = 1
		   NameMon = "Fishman Raider"
		   CFrameQuest = CFrame.new(-10581.6563, 333.41037, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
		   CFrameMon = CFrame.new(-10457.1738, 323.998352, -8450.38086, -1, 0, 0, 0, 1, 0, 0, 0, -1) 
		  
								  elseif MyLevel == 1800 or MyLevel <= 1824 then
			 Ms = "Fishman Captain [Lv. 1800]"
		   NaemQuest = "DeepForestIsland3"
		   
		   LevelQuest = 2
		   NameMon = "Fishman Captain"
		   CFrameQuest = CFrame.new(-10581.6563, 333.41037, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
		   CFrameMon = CFrame.new(-11120.0332, 313.449188, -8791.31348, -1, 0, 0, 0, 1, 0, 0, 0, -1) 
											 elseif MyLevel == 1825 or MyLevel <= 1849 then
			 Ms = "Forest Pirate [Lv. 1825]"
		   NaemQuest = "DeepForestIsland"
		   
		   LevelQuest = 1
		   NameMon = "Forest Pirate"
		   CFrameQuest = CFrame.new(-13234.04, 334.025909, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)
		   CFrameMon = CFrame.new(-13614.1426, 343.146973, -7756.50977, -0.515632391, 0, 0.856810033, 0, 1, 0, -0.856810033, 0, -0.515632391) 
													   elseif MyLevel == 1850 or MyLevel <= 1899 then
			 Ms = "Mythological Pirate [Lv. 1850]"
		   NaemQuest = "DeepForestIsland"
		   
		   LevelQuest = 2
		   NameMon = "Mythological Pirate"
		   CFrameQuest = CFrame.new(-13234.04, 334.025909, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)
		   CFrameMon = CFrame.new(-13681.8945, 420.407867, -7004.06641, -0.345898986, 0, 0.938271761, 0, 1, 0, -0.938271761, 0, -0.345898986) 
																  elseif MyLevel == 1900 or MyLevel <= 1924 then
			 Ms = "Jungle Pirate [Lv. 1900]"
		   NaemQuest = "DeepForestIsland2"
		   
		   LevelQuest = 1
		   NameMon = "Jungle Pirate"
		   CFrameQuest = CFrame.new(-12680.3818, 392.508453, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
		   CFrameMon = CFrame.new(-11861.918, 325.507813, -10098.6348, -1, 0, 0, 0, 1, 0, 0, 0, -1)
																			 elseif MyLevel >= 1925 then
			 Ms = "Musketeer Pirate [Lv. 1925]"
		   NaemQuest = "DeepForestIsland2"
		   
		   LevelQuest = 2
		   NameMon = "Musketeer Pirate"
		   CFrameQuest = CFrame.new(-12680.3818, 392.508453, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
		   CFrameMon = CFrame.new(-13457.0059, 386.467651, -9819.51953, 0.374604106, 0, 0.92718488, 0, 1, 0, -0.92718488, 0, 0.374604106) 
		end
	
	 end
  end
  
  ครบ 3 โลก
  
  TP หาCFrame ให้ละ ไปดูวิธีใช้ได้ที่  https://www.youtube.com/watch?v=w_TeN8S4E-U&t=203s
   if NewWorld then
	 Teleport:Button("First Island","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(82.9490662, 18.0710983, 2834.98779)
	 end)
	 Teleport:Button("Kingdom of Rose","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = game.Workspace["_WorldOrigin"].Locations["Kingdom of Rose"].CFrame
	 end)
	 Teleport:Button("Dark Ares","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = game.Workspace["_WorldOrigin"].Locations["Dark Arena"].CFrame
	 end)
	 Teleport:Button("Mansion","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-390.096313, 331.886475, 673.464966)
	 end)
	 Teleport:Button("Flamingo Room","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2302.19019, 15.1778421, 663.811035)
	 end)
	 Teleport:Button("Green bit","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2372.14697, 72.9919434, -3166.51416)
	 end)
	 Teleport:Button("Cafe","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-385.250916, 73.0458984, 297.388397)
	 end)
	 Teleport:Button("Factroy","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(430.42569, 210.019623, -432.504791)
	 end)
	 Teleport:Button("Colosseum","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1836.58191, 44.5890656, 1360.30652)
	 end)
	 Teleport:Button("Ghost Island","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5571.84424, 195.182297, -795.432922)
	 end)
	 Teleport:Button("Ghost Island 2nd","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5931.77979, 5.19706631, -1189.6908)
	 end)
	 Teleport:Button("Snow Mountain","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1384.68298, 453.569031, -4990.09766)
	 end)
	 Teleport:Button("Hot and Cold","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-6026.96484, 14.7461271, -5071.96338)
	 end)
	 Teleport:Button("Magma Side","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5478.39209, 15.9775667, -5246.9126)
	 end)
	 Teleport:Button("Cursed Ship","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(902.059143, 124.752518, 33071.8125)
	 end)
	 Teleport:Button("Frosted Island","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(5400.40381, 28.21698, -6236.99219)
	 end)
	 Teleport:Button("Forgotten Island","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-3043.31543, 238.881271, -10191.5791)
	 end)
	 Teleport:Button("Usoapp Island","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(4748.78857, 8.35370827, 2849.57959)
	 end)
	 Teleport:Button("Raids Low","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5554.95313, 329.075623, -5930.31396)
	 end)
	 Teleport:Button("Minisky Island","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-260.358917, 49325.7031, -35259.3008)
	 end)
  elseif OldWorld then
	  
	 Teleport:Button("Start Island","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1071.2832, 16.3085976, 1426.86792)
	 end)
	 Teleport:Button("Marine Start","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2573.3374, 6.88881969, 2046.99817)
	 end)
	 Teleport:Button("Middle Town","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-655.824158, 7.88708115, 1436.67908)
	 end)
	 Teleport:Button("Jungle","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1249.77222, 11.8870859, 341.356476)
	 end)
	 Teleport:Button("Pirate Village","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1122.34998, 4.78708982, 3855.91992)
	 end)
	 Teleport:Button("Desert","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1094.14587, 6.47350502, 4192.88721)
	 end)
	 Teleport:Button("Frozen Village","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1198.00928, 27.0074959, -1211.73376)
	 end)
	 Teleport:Button("Marine Ford","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-4505.375, 20.687294, 4260.55908)
	 end)
	 Teleport:Button("Colosseum","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1428.35474, 7.38933945, -3014.37305)
	 end)
	 Teleport:Button("Sky 1st","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-4970.21875, 717.707275, -2622.35449)
	 end)
	 Teleport:Button("Sky 2st ","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-4813.0249, 903.708557, -1912.69055)
	 end)
	 Teleport:Button("Sky 3st ","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-7952.31006, 5545.52832, -320.704956)
	 end)
	 Teleport:Button("Prison","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(4854.16455, 5.68742752, 740.194641)
	 end)
	 Teleport:Button("Magma Village","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5231.75879, 8.61593437, 8467.87695)
	 end)
	 Teleport:Button("UndeyWater City","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(61163.8516, 11.7796879, 1819.78418)
	 end)
	 Teleport:Button("Fountain City","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(5132.7124, 4.53632832, 4037.8562)
	 end)
	 Teleport:Button("House Cyborg's","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(6262.72559, 71.3003616, 3998.23047)
	 end)
	 Teleport:Button("Shank's Room","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1442.16553, 29.8788261, -28.3547478)
	 end)
	 Teleport:Button("Mob Island","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2850.20068, 7.39224768, 5354.99268)
	 end)
	 else
	Teleport:Button("First Island","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-325.113464, 40.1279297, 5491.7583, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
	end)
	 Teleport:Button("Boat Castle","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5419.64209, 310.163513, -2657.39526, 0.927179396, 0, 0.374617696, 0, 1, 0, -0.374617696, 0, 0.927179396)
	 end)
		  Teleport:Button("Marine Island","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5419.64209, 310.163513, -2657.39526, 0.927179396, 0, 0.374617696, 0, 1, 0, -0.374617696, 0, 0.927179396)
		  end)
		   Teleport:Button("Turtle Island","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-12916.8906, 327.117188, -7647.22168, -1, 0, 0, 0, 1, 0, 0, 0, -1)
		   end)
			Teleport:Button("Amazon Island","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(5832.79688, 53.2015953, -1101.43604, 0.898790359, -0, -0.438378751, 0, 1, -0, 0.438378751, 0, 0.898790359)
	 end)
	 Teleport:Button("Mini Sky","",function()
		game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-262.517487, 49321.5117, -35252.9375, -0.999392271, 0, 0.0348687991, 0, 1, 0, -0.0348687991, 0, -0.999392271)
	 end)  
 
