## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:210f20b2af7dc0b94dafa4087dbc16e27b546a2a1ea5edcb7fe94e60e641baa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull mongo@sha256:78a7d96aed14420d9c03a2abc53ccad188030363a88e4473ebfac04c1c11bac2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 MB (637770656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c61101812dd9c416bea70214ac479bae0d8ee0cdc09cb60bb59febf0fd6b99`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Thu, 18 Apr 2024 18:49:55 GMT
SHELL [cmd /S /C]
# Thu, 18 Apr 2024 18:49:56 GMT
USER ContainerAdministrator
# Thu, 18 Apr 2024 18:50:21 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 18 Apr 2024 18:50:21 GMT
USER ContainerUser
# Thu, 18 Apr 2024 18:50:23 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Thu, 18 Apr 2024 18:50:24 GMT
ENV MONGO_VERSION=6.0.15
# Thu, 18 Apr 2024 18:50:44 GMT
COPY dir:b68ff258c344bc8aa9f2b0f3549c715c1c93667ff42fef166146a10263a4fbca in C:\mongodb 
# Thu, 18 Apr 2024 18:51:03 GMT
RUN mongod --version
# Thu, 18 Apr 2024 18:51:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 18 Apr 2024 18:51:04 GMT
EXPOSE 27017
# Thu, 18 Apr 2024 18:51:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7147aa493486a46169d19cdc6d615a6b3b444828933705a9feafa5090e73d7ad`  
		Last Modified: Thu, 18 Apr 2024 18:51:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c39f4a4af2fdc2b6c6d9be255ea135cdb8145af73b040e07b1745cc74ee8a2b`  
		Last Modified: Thu, 18 Apr 2024 18:51:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08612dbb4146da7f8dbfe0ba66170187aa24b70dff0bec16d63255aa689a6381`  
		Last Modified: Thu, 18 Apr 2024 18:51:10 GMT  
		Size: 89.7 KB (89733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5111baa27607a1cf167abc451f418e2851546ce66f43731a018c562062dd7469`  
		Last Modified: Thu, 18 Apr 2024 18:51:11 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f664bf1e54ea99af0c66d993b0fb7b8ab288b04e0bef089b92f59ccb8625dad`  
		Last Modified: Thu, 18 Apr 2024 18:51:10 GMT  
		Size: 267.1 KB (267081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2c2b70d36a70c29e8edc2d523375401049811e3d826aa6811013346f5512ea`  
		Last Modified: Thu, 18 Apr 2024 18:51:10 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4751300f34de7c4927e61d0c805237e7f872b0c52500d295430f0ebad8cdbaba`  
		Last Modified: Thu, 18 Apr 2024 18:51:51 GMT  
		Size: 516.3 MB (516321166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44194a6c80f8cb4a4a4a5cfd13af346a6913978bc5e2f210c0ef513a537e426`  
		Last Modified: Thu, 18 Apr 2024 18:51:08 GMT  
		Size: 91.7 KB (91653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa5ff1d12ca2d929cae8daa8e3c266dc0997c81f1c57695ae76cb58f0a7c07d`  
		Last Modified: Thu, 18 Apr 2024 18:51:08 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c1f643cfd092f569989fff90ec0ab23c362f683e3a105b2dfb9f45c3d172a4`  
		Last Modified: Thu, 18 Apr 2024 18:51:08 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b1217e0c1ea632bfb75ca41c6e560645d74b0fb4e6c3cfd43f2516a215afc4`  
		Last Modified: Thu, 18 Apr 2024 18:51:08 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull mongo@sha256:bf9760bd5b92eabd282c60961b86c63a9853cd6a57d2fa130d8e643f0cf51ec8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.9 MB (622859600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce088c28520a0d3a2752ae922b9551015aea3f70932a44fa2bb931d08af282d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Thu, 18 Apr 2024 18:49:51 GMT
SHELL [cmd /S /C]
# Thu, 18 Apr 2024 18:49:52 GMT
USER ContainerAdministrator
# Thu, 18 Apr 2024 18:50:00 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 18 Apr 2024 18:50:01 GMT
USER ContainerUser
# Thu, 18 Apr 2024 18:50:03 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Thu, 18 Apr 2024 18:50:04 GMT
ENV MONGO_VERSION=6.0.15
# Thu, 18 Apr 2024 18:50:45 GMT
COPY dir:b68ff258c344bc8aa9f2b0f3549c715c1c93667ff42fef166146a10263a4fbca in C:\mongodb 
# Thu, 18 Apr 2024 18:50:56 GMT
RUN mongod --version
# Thu, 18 Apr 2024 18:50:56 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 18 Apr 2024 18:50:57 GMT
EXPOSE 27017
# Thu, 18 Apr 2024 18:50:58 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cf80505fea7a1d0d5ecbec9e45e5c2ef4ff27dbbdad7892323b756f690fb4b`  
		Last Modified: Thu, 18 Apr 2024 18:51:08 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d74c1b4823495cbe8027e0e4a0760aaae90c26d49336a2d32bccca7160db10b`  
		Last Modified: Thu, 18 Apr 2024 18:51:07 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b1f7ed04718380984e37f633eb6de0c892d90f152847a110b0edbadc3b1e89`  
		Last Modified: Thu, 18 Apr 2024 18:51:06 GMT  
		Size: 66.6 KB (66601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89df7e315fb26370fed7576fcd719e67be51af28b1199f2cb518f1ca2dbee56c`  
		Last Modified: Thu, 18 Apr 2024 18:51:06 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5316f75e10981f616517f26a43cfb955d7f36b5ea7c78c345d87e65e446959`  
		Last Modified: Thu, 18 Apr 2024 18:51:05 GMT  
		Size: 267.1 KB (267055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bfea539901c799bd6c498f5e7a9109a811b8b6cabe512dce7a0c6941933437`  
		Last Modified: Thu, 18 Apr 2024 18:51:05 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76cf5980499cabc3ff53cfffbd732ea1e5e17103b62f10acad04642207a760f`  
		Last Modified: Thu, 18 Apr 2024 18:51:46 GMT  
		Size: 516.3 MB (516321143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d496ed9cc8065aa542920a1ce4493090fb30c934b1a88d9149d42add4603299`  
		Last Modified: Thu, 18 Apr 2024 18:51:03 GMT  
		Size: 1.3 MB (1308392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6db8e4f875b1c91a0461c526ada42defabb8b0deddce2a81fe7ecf8f9dd3de`  
		Last Modified: Thu, 18 Apr 2024 18:51:03 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2e48fecc68e0cfc51d40b9221c3bd73d626c73898af63840b1c035d7e7167b`  
		Last Modified: Thu, 18 Apr 2024 18:51:03 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2483a9229ebd7fd7e14ff8eb2eb6ee83a45ad3396515488f7ddd96d4a03f1f`  
		Last Modified: Thu, 18 Apr 2024 18:51:03 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
