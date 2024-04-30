## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:f0def1bac1f2c1bc508fb4498b38130765c6f8465eb4e6f90cb686a9936bc83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull mongo@sha256:e84d15c33177dc425764f3ef53c434f2a02579dbaaf0dd1f587e3817c59fe2c6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.6 MB (738599116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e965aa60b2f07d24727fe1dd810179b5d082b01ec0eb5b7015bcf288d554e8d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Tue, 30 Apr 2024 00:53:03 GMT
SHELL [cmd /S /C]
# Tue, 30 Apr 2024 00:53:03 GMT
USER ContainerAdministrator
# Tue, 30 Apr 2024 00:53:21 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 30 Apr 2024 00:53:21 GMT
USER ContainerUser
# Tue, 30 Apr 2024 00:53:23 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Tue, 30 Apr 2024 00:53:23 GMT
ENV MONGO_VERSION=7.0.9
# Tue, 30 Apr 2024 00:53:51 GMT
COPY dir:c5adfa4f029ebda75c02b0a22ffb5e95f91770da0e60bc0d59f3d814db6f0d71 in C:\mongodb 
# Tue, 30 Apr 2024 00:54:10 GMT
RUN mongod --version
# Tue, 30 Apr 2024 00:54:11 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 30 Apr 2024 00:54:11 GMT
EXPOSE 27017
# Tue, 30 Apr 2024 00:54:12 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7aca7d546f3aeb542c760f25fa34556326354bddebe3e8cf7cb9eef89dd152`  
		Last Modified: Tue, 30 Apr 2024 00:54:20 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be5dd4521b26f575331663a1f05924c8af2162e0fcaf81087bcdcf39f1efc85`  
		Last Modified: Tue, 30 Apr 2024 00:54:20 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c78bc09f8e2e47954dd51a8494c79ed76f0b0c89732cef326264a221597d15`  
		Last Modified: Tue, 30 Apr 2024 00:54:18 GMT  
		Size: 106.7 KB (106740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bebb9e10c9b71b645f064fc871eff11c71822c056c57a5b401c931e4d68de1`  
		Last Modified: Tue, 30 Apr 2024 00:54:18 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11ab6227b7affac4a9c8556aec7678e5f930b0c3a6c87b5570a09b271d863de`  
		Last Modified: Tue, 30 Apr 2024 00:54:18 GMT  
		Size: 267.1 KB (267111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c652041ab99f5354b88b239fa0203177d4a19c952e1bf67c314825a082e8da`  
		Last Modified: Tue, 30 Apr 2024 00:54:18 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e633ab745d25469d5a8ffe4b727745a87924e5cdcff94755db4471c99dc583`  
		Last Modified: Tue, 30 Apr 2024 00:55:08 GMT  
		Size: 617.1 MB (617115357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fb7a96530720921d111b95ecd329454a27a939bae7159cb2bef57567e7e0d9`  
		Last Modified: Tue, 30 Apr 2024 00:54:16 GMT  
		Size: 108.9 KB (108881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bd1c3a2fa18b076768c66e1331fb7e910c4392e1f73c76116cf29cfd1625c4`  
		Last Modified: Tue, 30 Apr 2024 00:54:16 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c6c38fc131d43a29b81f998afbe1710e6e5f30c43571770187bed832838ac0`  
		Last Modified: Tue, 30 Apr 2024 00:54:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0965ada1ea428c402e1875fbd0d40801ecec76845abdc851cd638607288fbba`  
		Last Modified: Tue, 30 Apr 2024 00:54:16 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull mongo@sha256:0a53857643d0666be903ca180c24aaf32c4767290cd3440a4ad7a50a70ea6a91
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 MB (722420402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d867c6b2448fe7ccb78dca84a3086c3d58e3268b86ada4ff20c17be43190a8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 30 Apr 2024 00:53:15 GMT
SHELL [cmd /S /C]
# Tue, 30 Apr 2024 00:53:17 GMT
USER ContainerAdministrator
# Tue, 30 Apr 2024 00:53:39 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 30 Apr 2024 00:53:39 GMT
USER ContainerUser
# Tue, 30 Apr 2024 00:53:42 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Tue, 30 Apr 2024 00:53:43 GMT
ENV MONGO_VERSION=7.0.9
# Tue, 30 Apr 2024 00:54:29 GMT
COPY dir:c5adfa4f029ebda75c02b0a22ffb5e95f91770da0e60bc0d59f3d814db6f0d71 in C:\mongodb 
# Tue, 30 Apr 2024 00:54:37 GMT
RUN mongod --version
# Tue, 30 Apr 2024 00:54:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 30 Apr 2024 00:54:38 GMT
EXPOSE 27017
# Tue, 30 Apr 2024 00:54:39 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991502ff9da4715db7dafae1cae7438823871818253b7ba2406fc21cb4c3fb26`  
		Last Modified: Tue, 30 Apr 2024 00:54:44 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e684e1245202576ed814f0e8ecb9aa428ae6a2d869623fab9e31173210ab3c`  
		Last Modified: Tue, 30 Apr 2024 00:54:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b98a4f073167c740688e2cb7527832efeece29c1fec7fc07516b3fced3b8fb`  
		Last Modified: Tue, 30 Apr 2024 00:54:43 GMT  
		Size: 67.9 KB (67914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2003242458d5ceaa21200676a184a915ad170187c600cdf12d2575c97296cbe0`  
		Last Modified: Tue, 30 Apr 2024 00:54:42 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28810f8898a9a0864599fca902c6316d49b8eb61a5ad929be0bbcda8ee22fe7f`  
		Last Modified: Tue, 30 Apr 2024 00:54:43 GMT  
		Size: 267.1 KB (267057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502a37b4a8160ec54bac5a1e224c700d9746f73667bc03fe7e6a986dca4cb8ce`  
		Last Modified: Tue, 30 Apr 2024 00:54:43 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffdd5372ea6f6d56b733610d5ce522e0ff6126f7ce1b38204a73a1c92af40af`  
		Last Modified: Tue, 30 Apr 2024 00:55:32 GMT  
		Size: 617.1 MB (617115347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d05f891781373270b3d5518cc098b48aae42d09821188be42b807e7fc361d1`  
		Last Modified: Tue, 30 Apr 2024 00:54:41 GMT  
		Size: 73.7 KB (73749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f3c628e79b84984a75f7cdc018177826387418a3cc3df11c771fe142666411`  
		Last Modified: Tue, 30 Apr 2024 00:54:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00c40ac7cc5b2cef04deeecbca0325dc43f85ef54f70ea05c0f092c99fb68b4`  
		Last Modified: Tue, 30 Apr 2024 00:54:41 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ada796b0fb5bae1b18cd757338752d6934de5c0ef174746ab760de5862d586`  
		Last Modified: Tue, 30 Apr 2024 00:54:42 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
