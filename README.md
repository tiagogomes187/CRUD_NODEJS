# CRUD COM NODEJS PARA GEEKHUNTER

Este código contém comentários, para verificar uma versão sem comentários clique aqui [clique aqui](https://gist.github.com/brendonguedes/a80a11dc7979bbc8fbece728976de0f0)

Imagem do código sem comentários no Carbon. ![Markdown](https://carbon.now.sh/?bg=rgba(144%252C19%252C254%252C1)&t=dracula&wt=none&l=javascript&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=14px&lh=133%2525&si=false&es=4x&wm=false&code=const%252520express%252520%25253D%252520require('express')%25253B%25250A%25250Aconst%252520server%252520%25253D%252520express()%25253B%25250A%25250Aserver.use(express.json())%25253B%25250A%25250Aconst%252520geeks%252520%25253D%252520%25255B'Brendon'%25252C%252520'Lara'%25252C%252520'Gregory'%25252C%252520'Hunter'%25255D%25253B%25250A%25250Aserver.use((req%25252C%252520res%25252C%252520next)%252520%25253D%25253E%252520%25257B%25250A%252520%252520%25250A%252520%252520console.time('Request')%25253B%25250A%252520%252520console.log(%252560M%2525C3%2525A9todo%25253A%252520%252524%25257Breq.method%25257D%25253B%252520URL%25253A%252520%252524%25257Breq.url%25257D%25253B%252520%252560)%25253B%25250A%252520%252520%25250A%252520%252520next()%25253B%25250A%25250A%252520%252520console.log('Finalizou')%25253B%25250A%252520%252520console.timeEnd('Request')%25253B%25250A%25257D)%25253B%25250A%25250Afunction%252520checkGeekExists(req%25252C%252520res%25252C%252520next)%252520%25257B%25250A%252520%252520if%252520(!req.body.name)%252520%25257B%25250A%252520%252520%252520%252520return%252520res.status(400).json(%25257B%252520error%25253A%252520'geek%252520name%252520is%252520required'%252520%25257D)%25253B%252520%252520%252520%252520%25250A%252520%252520%25257D%25250A%252520%252520return%252520next()%25253B%25250A%25257D%252520%25250A%252520%252520%25250Afunction%252520checkGeekInArray(req%25252C%252520res%25252C%252520next)%252520%25257B%25250A%252520%252520const%252520geek%252520%25253D%252520geeks%25255Breq.params.index%25255D%25253B%25250A%252520%252520if%252520(!geek)%252520%25257B%25250A%252520%252520%252520%252520return%252520res.status(400).json(%25257B%252520error%25253A%252520'geek%252520does%252520not%252520exists'%252520%25257D)%25253B%25250A%252520%252520%25257D%25250A%252520%252520req.geek%252520%25253D%252520geek%25253B%25250A%25250A%252520%252520return%252520next()%25253B%25250A%25257D%25250A%25250Aserver.get('%25252Fgeeks'%25252C%252520(req%25252C%252520res)%252520%25253D%25253E%252520%25257B%25250A%252520%252520return%252520res.json(geeks)%25253B%25250A%25257D)%25250A%25250Aserver.get('%25252Fgeeks%25252F%25253Aindex'%25252C%252520checkGeekInArray%25252C%252520(req%25252C%252520res)%252520%25253D%25253E%252520%25257B%25250A%252520%252520return%252520res.json(req.geek)%25253B%25250A%25257D)%25250A%25250Aserver.post('%25252Fgeeks'%25252C%252520checkGeekExists%25252C%252520(req%25252C%252520res)%252520%25253D%25253E%252520%25257B%25250A%252520%252520const%252520%25257B%252520name%252520%25257D%252520%25253D%252520req.body%25253B%25250A%252520%252520geeks.push(name)%25253B%25250A%252520%252520return%252520res.json(geeks)%25253B%25250A%25257D)%25250A%25250Aserver.put('%25252Fgeeks%25252F%25253Aindex'%25252C%252520checkGeekInArray%25252C%252520checkGeekExists%25252C%252520(req%25252C%252520res)%252520%25253D%25253E%252520%25257B%25250A%252520%252520const%252520%25257B%252520index%252520%25257D%252520%25253D%252520req.params%25253B%25250A%252520%252520const%252520%25257B%252520name%252520%25257D%252520%25253D%252520req.body%25253B%25250A%252520%252520geeks%25255Bindex%25255D%252520%25253D%252520name%25253B%25250A%252520%252520return%252520res.json(geeks)%25253B%25250A%25257D)%25253B%25250A%25250Aserver.delete('%25252Fgeeks%25252F%25253Aindex'%25252C%252520checkGeekInArray%25252C%252520(req%25252C%252520res)%252520%25253D%25253E%252520%25257B%25250A%252520%252520const%252520%25257B%252520index%252520%25257D%252520%25253D%252520req.params%25253B%25250A%25250A%252520%252520geeks.splice(index%25252C%2525201)%25253B%25250A%252520%252520return%252520res.send()%25253B%25250A%25257D)%25253B%25250A%25250Aserver.listen(3000)%25253B%25250A%25250A%25252F%25252F%252520CRUD%252520with%252520NODEJS%252520developed%252520by%252520Brendon%252520Guedes%252520%2525F0%25259F%252592%25259C)

