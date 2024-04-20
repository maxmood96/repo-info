## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:24284c50daaa2065481ebbc92c5cd56368ff6c5f2ce5b8ba7cc411672aa5dc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.5696; amd64

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
