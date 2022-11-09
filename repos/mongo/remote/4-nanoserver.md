## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:7af41fc511970436f58b64be94b58713263634906a84b02f0e86a2773b1ac5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.1249; amd64

```console
$ docker pull mongo@sha256:4522523547ce1bac1fe32456dcaaf2f65d7456bc344a575403590487b9723768
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366710398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba2379486fc16a3719e8f41a60c05e4993cc8470c395d3bbb44106dccf19f0e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Nov 2022 07:21:30 GMT
RUN Apply image 10.0.20348.1249
# Wed, 09 Nov 2022 14:03:51 GMT
SHELL [cmd /S /C]
# Wed, 09 Nov 2022 18:28:15 GMT
USER ContainerAdministrator
# Wed, 09 Nov 2022 18:28:35 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 09 Nov 2022 18:28:36 GMT
USER ContainerUser
# Wed, 09 Nov 2022 18:36:29 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 09 Nov 2022 18:43:34 GMT
ENV MONGO_VERSION=4.4.17
# Wed, 09 Nov 2022 18:44:01 GMT
COPY dir:cdbba282fa1cacd2b09d4c40c2e879c5f3979f218aaa5472d9e47359ab0a3a21 in C:\mongodb 
# Wed, 09 Nov 2022 18:44:20 GMT
RUN mongo --version && mongod --version
# Wed, 09 Nov 2022 18:44:21 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Nov 2022 18:44:22 GMT
EXPOSE 27017
# Wed, 09 Nov 2022 18:44:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:72e5d750fe8c1a32d4a26ef3b4a4e1f6124ac079b142f12724af2abfcba1c8b3`  
		Last Modified: Tue, 08 Nov 2022 19:57:58 GMT  
		Size: 122.1 MB (122092167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5798382a92edbf13363f09d29194b10dba5ce50456d5499d8b33a42e2c702cd`  
		Last Modified: Wed, 09 Nov 2022 14:34:17 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fa4dc6ee264fdf67c57b4158cf6e575cb0a820aa5dbb991e3f333d2202307b`  
		Last Modified: Wed, 09 Nov 2022 19:06:19 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980b091f06a8d628071da46b850437b7a38c09046802ff108c9aff1d62451525`  
		Last Modified: Wed, 09 Nov 2022 19:06:16 GMT  
		Size: 86.9 KB (86878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0725d6d4e52a7894c3c2a870fd0f22b94e68d055eae2cc57a75b9b41ea6318`  
		Last Modified: Wed, 09 Nov 2022 19:06:16 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefabfbbe03c334aba82e08dee17043a6c00406655e5fc13a72554e0ae7b4cfc`  
		Last Modified: Wed, 09 Nov 2022 19:12:12 GMT  
		Size: 263.5 KB (263495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944783ad76cb725f734b74a37a9527577430719169449701b67aa09db34ecf60`  
		Last Modified: Wed, 09 Nov 2022 19:16:45 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68cff85c8cbc6762711e6d7f183a194950ffffc0d140d1e43a0d037e4f00a4c`  
		Last Modified: Wed, 09 Nov 2022 19:17:30 GMT  
		Size: 244.2 MB (244210383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c691167094d91349f5edb3032f3d7d3561f52488f8e33dcf55a7f1b636f517e`  
		Last Modified: Wed, 09 Nov 2022 19:16:43 GMT  
		Size: 49.4 KB (49359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9071c07a8833c6784f4ff431315507ca38e1f953e1d3836dba8c67895cc82d6d`  
		Last Modified: Wed, 09 Nov 2022 19:16:43 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0308c4c3ad68f32357cf0e9a37dcf37167245ab100955013931319ebdd0a435b`  
		Last Modified: Wed, 09 Nov 2022 19:16:43 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989321394ffddc4f3cee6b36149b8956d47a088f37807bf72fc815f2db745cf9`  
		Last Modified: Wed, 09 Nov 2022 19:16:43 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull mongo@sha256:f0b60b5541579a674c2347b151fc00b1294c37678839b3ce53e86b4bec82cbc2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 MB (351355310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c2fda07843b96244bd97ccc3ab1cfb34efeb040f235f045c10e27d5f728b30`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 14:09:15 GMT
SHELL [cmd /S /C]
# Wed, 09 Nov 2022 18:30:00 GMT
USER ContainerAdministrator
# Wed, 09 Nov 2022 18:30:15 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 09 Nov 2022 18:30:16 GMT
USER ContainerUser
# Wed, 09 Nov 2022 18:37:49 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 09 Nov 2022 18:44:37 GMT
ENV MONGO_VERSION=4.4.17
# Wed, 09 Nov 2022 18:45:01 GMT
COPY dir:cdbba282fa1cacd2b09d4c40c2e879c5f3979f218aaa5472d9e47359ab0a3a21 in C:\mongodb 
# Wed, 09 Nov 2022 18:45:18 GMT
RUN mongo --version && mongod --version
# Wed, 09 Nov 2022 18:45:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Nov 2022 18:45:19 GMT
EXPOSE 27017
# Wed, 09 Nov 2022 18:45:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83e42a06a19f2d133476fa58d61bf56ed65a782146e4f8b37b3fc8727440fbd`  
		Last Modified: Wed, 09 Nov 2022 14:35:26 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6449712c858131bae1c7bddbe1897bb48c821a1169952834ef9364fee0384db`  
		Last Modified: Wed, 09 Nov 2022 19:08:05 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e914de04c2af4eb226e2cb7b4bbcf383cb62175d5df12dbcc9b03bba182e41`  
		Last Modified: Wed, 09 Nov 2022 19:08:02 GMT  
		Size: 71.4 KB (71358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca05487e297333fc707a0a3c04d76f9c45b34ab868772e71f7eebbd106664df`  
		Last Modified: Wed, 09 Nov 2022 19:08:02 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635580a42bba22cbe74bf589efb5ed78d794665d909c36216aea3d718da59b7e`  
		Last Modified: Wed, 09 Nov 2022 19:13:23 GMT  
		Size: 263.5 KB (263460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c38755548234b82488a0eed5aeb7f56ca392483dfa4bae2c03d9d841b33712`  
		Last Modified: Wed, 09 Nov 2022 19:17:46 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacdd59fa731f557cb7680fd7c3d3a345e41bb683e12dcf41e1cfb43ef6c98ab`  
		Last Modified: Wed, 09 Nov 2022 19:18:31 GMT  
		Size: 244.2 MB (244210336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8783ac8f0b4211c677961c1d749fef13aad2df592b0f2f335363c46d34175`  
		Last Modified: Wed, 09 Nov 2022 19:17:44 GMT  
		Size: 78.4 KB (78392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfdd29b85ade5b9f19b197af15fa1e49d02083e3666fd36d8e558e7de334b43`  
		Last Modified: Wed, 09 Nov 2022 19:17:44 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5649eaf4b2c1e3ecb4a4c631f05159fb58b301a589686919e30720face8916f`  
		Last Modified: Wed, 09 Nov 2022 19:17:44 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2fa4bfea7d73adb6e4ea5110a38411c61792132d199bc660a97f36702ac1b9`  
		Last Modified: Wed, 09 Nov 2022 19:17:44 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
