## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:86cc1b2a80ce58ebd664b3469ec9e921052c3300acd55afbfb8bdbeff6c4cacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.2461; amd64

```console
$ docker pull mongo@sha256:4124bacf69d49924c6d242263bca476c322172e25604aad70065f8f7fb04de60
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.0 MB (737966110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1e948544e283d31594388a6e7d2b9e514330c6ef95c59c0486361d4f65b224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Wed, 15 May 2024 22:52:43 GMT
SHELL [cmd /S /C]
# Wed, 15 May 2024 22:52:43 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 22:53:14 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 May 2024 22:53:15 GMT
USER ContainerUser
# Wed, 15 May 2024 22:53:17 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 15 May 2024 22:53:18 GMT
ENV MONGO_VERSION=7.0.9
# Wed, 15 May 2024 22:53:46 GMT
COPY dir:c5adfa4f029ebda75c02b0a22ffb5e95f91770da0e60bc0d59f3d814db6f0d71 in C:\mongodb 
# Wed, 15 May 2024 22:54:06 GMT
RUN mongod --version
# Wed, 15 May 2024 22:54:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 May 2024 22:54:08 GMT
EXPOSE 27017
# Wed, 15 May 2024 22:54:08 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d4fc5421c6de617379092fad8738bc94c009a465e43ad66b2f8e6285b28101`  
		Last Modified: Wed, 15 May 2024 22:54:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8a54f181eec98f9580c299c72fb350de710fdbd19c714b6a36c9f3c434dba8`  
		Last Modified: Wed, 15 May 2024 22:54:13 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28eb3a793e19fe5eb3c32eee5783bbb87474741d8fd10139a6bae8bf0fda30b2`  
		Last Modified: Wed, 15 May 2024 22:54:12 GMT  
		Size: 71.7 KB (71702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfdcf24154681aef0f67fba0215ca6664b732bdb86a09a916579ba58e721b21`  
		Last Modified: Wed, 15 May 2024 22:54:12 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3468db74dd871574bffd163f56faa41e6b21a1ac36013fda72a999f6b6535083`  
		Last Modified: Wed, 15 May 2024 22:54:12 GMT  
		Size: 267.1 KB (267085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14d7dde323f195908c62f4704cc6de121060d65b779177eefec026bb38f9b1a`  
		Last Modified: Wed, 15 May 2024 22:54:12 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c45b515c9ade7925f4d0fdb67a439dfe56dee7df95fd8f645978e3a48755c8`  
		Last Modified: Wed, 15 May 2024 22:55:01 GMT  
		Size: 617.1 MB (617115185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb55abe78c315388b29e365395e33be72aa55c8966845d598b9de539109c9700`  
		Last Modified: Wed, 15 May 2024 22:54:11 GMT  
		Size: 79.4 KB (79444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d0feab076c408d8bf0a56729e2de7a5cec2465a91b03119d658415e0ce0878`  
		Last Modified: Wed, 15 May 2024 22:54:11 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4289354f1888e4959bd4546946db7f1351f50d86f76eceed22a87b85bb0cb45`  
		Last Modified: Wed, 15 May 2024 22:54:11 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b7d05e3729907978b4cab2665cf7650bdad15c8fe80dd4df2c2160c1d0c270`  
		Last Modified: Wed, 15 May 2024 22:54:11 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull mongo@sha256:2741be5637b5f5f6ecd6abadb1b6a9100d0daccaef1e248e3addbb5bab54697d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **773.6 MB (773647247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467bed719c7a10d2fe869616db1a7b1611614f6fbc592ebc943419abbe9fa423`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 22:52:56 GMT
SHELL [cmd /S /C]
# Wed, 15 May 2024 22:52:57 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 22:53:07 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 May 2024 22:53:08 GMT
USER ContainerUser
# Wed, 15 May 2024 22:53:10 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 15 May 2024 22:53:11 GMT
ENV MONGO_VERSION=7.0.9
# Wed, 15 May 2024 22:53:51 GMT
COPY dir:c5adfa4f029ebda75c02b0a22ffb5e95f91770da0e60bc0d59f3d814db6f0d71 in C:\mongodb 
# Wed, 15 May 2024 22:54:08 GMT
RUN mongod --version
# Wed, 15 May 2024 22:54:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 May 2024 22:54:09 GMT
EXPOSE 27017
# Wed, 15 May 2024 22:54:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27e67108a9a52d9fd442a062d2ad5621246bb73f2161a3a7dd03ceb16fc3504`  
		Last Modified: Wed, 15 May 2024 22:54:14 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10ea7e81d4c623e54564741ceab1ecfb714a968d38dc6757400984e476b6e89`  
		Last Modified: Wed, 15 May 2024 22:54:13 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3e040bda1637cf6d88be93729a917da7e8bee7c1694b1727c91425cb852eb4`  
		Last Modified: Wed, 15 May 2024 22:54:13 GMT  
		Size: 67.1 KB (67112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8c69bc0e7347f2917f230c300d30f76aee97ba47a347b5829161fecba69b96`  
		Last Modified: Wed, 15 May 2024 22:54:13 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e734c87ced37b6b4e6e31c53d15288ef00ccfa021821acbd1cb765f69f0a37d5`  
		Last Modified: Wed, 15 May 2024 22:54:12 GMT  
		Size: 267.1 KB (267074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75b4a17b2b5e796dcbac18f401a9a53ac7a9583580aa3f25d9d94a3c778b095`  
		Last Modified: Wed, 15 May 2024 22:54:12 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc6370ff35f574a8c946a3fef13f7c19fc7a76bdad6cc3680e91cc5ecefd67f`  
		Last Modified: Wed, 15 May 2024 22:55:02 GMT  
		Size: 617.1 MB (617115248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac937cacbb3e6a87bf0f706ea9e6b5f47a6895ea9150c56994967a09f5700b5c`  
		Last Modified: Wed, 15 May 2024 22:54:12 GMT  
		Size: 1.2 MB (1249124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0002eab1dd510287b1254cd5c18abc28efcfdbd5a98fdaff12ad50944ed8c356`  
		Last Modified: Wed, 15 May 2024 22:54:11 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac72d09fd95be060a44d7e4561c5c14ea4142980db949b9b6baf8b28c8fb7a9a`  
		Last Modified: Wed, 15 May 2024 22:54:11 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e1025753dee622af6c28c7109bd670af0a162da400eb9e452fe74e697f7613`  
		Last Modified: Wed, 15 May 2024 22:54:11 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
