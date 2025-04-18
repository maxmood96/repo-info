## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:c4cb804a9f7d02ab00f431e50cd852f0f0aaa699644295c3fd80f0c5feb7e83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull mongo@sha256:8a8b331032056e6d7a6f92e6cd038fb307025d226f127f61fb84e37c6d14f1f9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.9 MB (648864059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697f562744c4076fda6ac0a9dad80f23423bade2dc9bb7a0c728c7f4f2848a91`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:19:49 GMT
SHELL [cmd /S /C]
# Fri, 18 Apr 2025 04:19:50 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:19:52 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 18 Apr 2025 04:19:53 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:19:54 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Fri, 18 Apr 2025 04:19:55 GMT
ENV MONGO_VERSION=6.0.22
# Fri, 18 Apr 2025 04:20:12 GMT
COPY dir:4b15d5e4d896c710da0908054bfc1acda67a6afe024035e1b165242aea0e7d87 in C:\mongodb 
# Fri, 18 Apr 2025 04:20:24 GMT
RUN mongod --version
# Fri, 18 Apr 2025 04:20:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 04:20:26 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 04:20:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7a9911b10768e85ce7baac34fd650529642a8e92df23f00178ea7be65bdeda`  
		Last Modified: Fri, 18 Apr 2025 04:20:33 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d26f26432eec6f54915af8a7ae2aaacbb39295269bbf9f0b54f08436a68021`  
		Last Modified: Fri, 18 Apr 2025 04:20:33 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fceba58bc696e2e8b5ee33ec417c4ab77a8632347356dd91001d781baf21af5`  
		Last Modified: Fri, 18 Apr 2025 04:20:31 GMT  
		Size: 75.9 KB (75931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7870bc8cabf468cfeec8fa58567f36306e352855d9391c6d2c235e3a7c43548`  
		Last Modified: Fri, 18 Apr 2025 04:20:31 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c145ab2cd4edd6749d40c4b1976079ca37334aa31c8e74c8013086ffa40a7f`  
		Last Modified: Fri, 18 Apr 2025 04:20:31 GMT  
		Size: 275.2 KB (275167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583249df4ff7dd267ad4d9030d566000e0382c8ff5f0e51764cebccba14427d3`  
		Last Modified: Fri, 18 Apr 2025 04:20:31 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92752e526c3227220fa5e811d2a2e671762aade6db9992079d066796cdad0ab4`  
		Last Modified: Fri, 18 Apr 2025 04:21:15 GMT  
		Size: 525.9 MB (525872257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ee5a5b3f66512a3488dc1878edf68a554a71b554f7a5e2e9bcb0a7f96ccd15`  
		Last Modified: Fri, 18 Apr 2025 04:20:30 GMT  
		Size: 94.4 KB (94424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21be0bd93c93a5d39a0a994e11f500c17389b1e4a4bec4372eb5e1ce09bdf0bb`  
		Last Modified: Fri, 18 Apr 2025 04:20:30 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778c274b56e7ec874279a6e929aa1af4a27923000fd0a5fa1bfc92933b21fe60`  
		Last Modified: Fri, 18 Apr 2025 04:20:30 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f88c7b035529b7ab156aa0a2d103c25b8eff372975610b4a2b1759da85b255`  
		Last Modified: Fri, 18 Apr 2025 04:20:30 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull mongo@sha256:8e20719e907efcbff9de5ca24e07b3576c3cca9ef62e5bfff20f307b4058ce6d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.0 MB (635048851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb9777af3b91454d2facc0393a049f85749862e543212fe9a65bf3d5ab9cdfa`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:14:12 GMT
SHELL [cmd /S /C]
# Fri, 18 Apr 2025 04:14:14 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:14:16 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 18 Apr 2025 04:14:17 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:14:18 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Fri, 18 Apr 2025 04:14:19 GMT
ENV MONGO_VERSION=6.0.22
# Fri, 18 Apr 2025 04:14:45 GMT
COPY dir:4b15d5e4d896c710da0908054bfc1acda67a6afe024035e1b165242aea0e7d87 in C:\mongodb 
# Fri, 18 Apr 2025 04:14:54 GMT
RUN mongod --version
# Fri, 18 Apr 2025 04:14:55 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 04:14:56 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 04:14:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a217ef2c14ddb1617ee1c73dfd1e1186ef6365e2b53480b0fc1b253c45215f1b`  
		Last Modified: Fri, 18 Apr 2025 04:15:05 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313865cdf488ec7e3ca94226873a9cebc3244fd40f2870fcd54a412794ca387d`  
		Last Modified: Fri, 18 Apr 2025 04:15:04 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf68ece530668fc32ba82eb722b317395e8369d8189adb959faed4be96fde45`  
		Last Modified: Fri, 18 Apr 2025 04:15:03 GMT  
		Size: 69.1 KB (69108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80048f725578fb50c83c9069a2a8d92e44dcc14169e4343b3491d72e8a3c2032`  
		Last Modified: Fri, 18 Apr 2025 04:15:03 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af919deccf2a7bf135633fb3b7ec0241838024812e9005938718268a8f298582`  
		Last Modified: Fri, 18 Apr 2025 04:15:03 GMT  
		Size: 275.2 KB (275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a678f1a41bc35fd17720b472924821ea5ce94091dd0382b4bb6b6f2bb584c2f`  
		Last Modified: Fri, 18 Apr 2025 04:15:03 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230bb7569d373d83bbda50fdec870456fdc72ddbf894bf059a39a8e21b034f68`  
		Last Modified: Fri, 18 Apr 2025 04:15:44 GMT  
		Size: 525.9 MB (525872205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ee42cfff1a897028e3ec54baf812ccb5760ce50ec2235760acd03f4f269fa5`  
		Last Modified: Fri, 18 Apr 2025 04:15:01 GMT  
		Size: 72.9 KB (72864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb10debbd380ae6d65c9e7abf96ab3e371b422627dadcecce5c9a2bf3ab132cf`  
		Last Modified: Fri, 18 Apr 2025 04:15:01 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec97cda5ecef6cd5b7fd19fbe03f7acafe058b925801535a5d559c733c31eea3`  
		Last Modified: Fri, 18 Apr 2025 04:15:01 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1227b058a93a49c7052da824993bc0e642d8306c809c6ad7ac6f5b2001abf840`  
		Last Modified: Fri, 18 Apr 2025 04:15:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
