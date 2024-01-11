## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:d0c6c3583fc03e4b05418bc00456d81cb1800c6b402604e276e8d3e0efc68553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull mongo@sha256:3e2ade023ca7da0d603557792310cd56b59d750aefd1596470b18ccd8d0865a4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.6 MB (638622051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8519f7e226dc3416b4387810d920884caefe32f8b4181486c20a851432fa3e2a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Thu, 11 Jan 2024 00:56:32 GMT
SHELL [cmd /S /C]
# Thu, 11 Jan 2024 00:56:33 GMT
USER ContainerAdministrator
# Thu, 11 Jan 2024 00:56:35 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 11 Jan 2024 00:56:36 GMT
USER ContainerUser
# Thu, 11 Jan 2024 00:56:37 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Thu, 11 Jan 2024 00:56:38 GMT
ENV MONGO_VERSION=6.0.12
# Thu, 11 Jan 2024 00:57:11 GMT
COPY dir:329dc1f21a61007915141205ec19b27dc3ea273dd304d374db84e0d8d0974daa in C:\mongodb 
# Thu, 11 Jan 2024 00:57:19 GMT
RUN mongod --version
# Thu, 11 Jan 2024 00:57:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jan 2024 00:57:20 GMT
EXPOSE 27017
# Thu, 11 Jan 2024 00:57:21 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca950e8c258b0513283208d8fde8a1afbe437f695a13d79d32a602265e407b0`  
		Last Modified: Thu, 11 Jan 2024 00:57:25 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6515f93b0d79741632476d5da3deb2cb9bac7362e9681a64fb086360eba64364`  
		Last Modified: Thu, 11 Jan 2024 00:57:25 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9cd825611778cd9f3fc4a87b97758580b62674a74bd9db624e9a17015d4662`  
		Last Modified: Thu, 11 Jan 2024 00:57:25 GMT  
		Size: 86.9 KB (86915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f702121ec99e212eeb82afeca4e7cb6ef8f6e2d90176dcaefd9a0468703facd`  
		Last Modified: Thu, 11 Jan 2024 00:57:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519cb7e5aef08a7afa66e801404f4e0d76b6e284392f2a58bae9921d960dbfb0`  
		Last Modified: Thu, 11 Jan 2024 00:57:24 GMT  
		Size: 267.1 KB (267069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08e8087e977dfff486ec636cf90a1c839c4b3292bc514938c3b811050285078`  
		Last Modified: Thu, 11 Jan 2024 00:57:24 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea95b85512b4329f2cd7b95d48c611d911764a749b5961ef3e969e3b7da0271`  
		Last Modified: Thu, 11 Jan 2024 00:58:05 GMT  
		Size: 517.4 MB (517399514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc42c6205b59601fb4d5358ff39fc55736a42c939b77bf4c6424340502bd61f`  
		Last Modified: Thu, 11 Jan 2024 00:57:23 GMT  
		Size: 92.0 KB (92013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b044365eefee22805efc4c9e1b4e3bf200105ad9c0a50334010fc5703eb0eb`  
		Last Modified: Thu, 11 Jan 2024 00:57:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fbd490d952519183b3ff0ccd2c0f367551e1e4834e2ee9d500deb4b33f1096`  
		Last Modified: Thu, 11 Jan 2024 00:57:23 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2422c8e7f07f0d7128842bae812ba713f8a4da848421b5e04ec7b8c03c5b38d`  
		Last Modified: Thu, 11 Jan 2024 00:57:23 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
