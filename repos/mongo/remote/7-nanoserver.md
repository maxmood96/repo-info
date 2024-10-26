## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:f7ba9f697e6ba942a0a5c7813f740c0c58ffe2eaaecca7d4b74d60a31baa7ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull mongo@sha256:c5a8a33cda41408ac47b7d700b2d0bdd0cb9b937af2e9ce85716428921a4a2f7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.3 MB (731311324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ea38f66520a1658e2016ad96a3321e5641395211f3e1c8bb44d15bc3a9dd90`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Sat, 26 Oct 2024 00:49:43 GMT
SHELL [cmd /S /C]
# Sat, 26 Oct 2024 00:49:43 GMT
USER ContainerAdministrator
# Sat, 26 Oct 2024 00:50:06 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 26 Oct 2024 00:50:06 GMT
USER ContainerUser
# Sat, 26 Oct 2024 00:50:08 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 26 Oct 2024 00:50:09 GMT
ENV MONGO_VERSION=7.0.15
# Sat, 26 Oct 2024 00:50:29 GMT
COPY dir:420a97257b8f41b5187b8c509722525c37efef8c1a1591fc20aa57d257fef5d8 in C:\mongodb 
# Sat, 26 Oct 2024 00:50:46 GMT
RUN mongod --version
# Sat, 26 Oct 2024 00:50:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 26 Oct 2024 00:50:47 GMT
EXPOSE 27017
# Sat, 26 Oct 2024 00:50:48 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18294ae42c7394e932458dbb1db7da9e78440e7f1c4dcd68a792e021e04e1b2`  
		Last Modified: Sat, 26 Oct 2024 00:50:52 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c03c8477c63e51c8ef1d8e93b563cdfd2df6fe37d15acc4088ca81dbf328e2`  
		Last Modified: Sat, 26 Oct 2024 00:50:52 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33383ec54d50c1d558fb63a6f3cd01e95371bd4a816f53a9df2ec5c5a6884b1a`  
		Last Modified: Sat, 26 Oct 2024 00:50:51 GMT  
		Size: 88.8 KB (88789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060036e0de059bc174be5240e44efb4f68a2bb682a2fa08ed3e132a71b681b6d`  
		Last Modified: Sat, 26 Oct 2024 00:50:51 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71ee23a42810ac9787d00d6eb1849e3542d52cf0b4fe292111f1cd9f61ce0fb`  
		Last Modified: Sat, 26 Oct 2024 00:50:51 GMT  
		Size: 275.2 KB (275154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a34734b38fe03ee397649d5e6e1ebb730f83b31727efe13a5d78fd215925d1c`  
		Last Modified: Sat, 26 Oct 2024 00:50:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618acaaa1b0226945645bb38eacd9f0da7d568b34006c020c45ec7fa64142b19`  
		Last Modified: Sat, 26 Oct 2024 00:51:38 GMT  
		Size: 610.3 MB (610337562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb939080d7ae3c172d7484a31c4b93d9e61eeba8699c5ded3e6a65ac7da68115`  
		Last Modified: Sat, 26 Oct 2024 00:50:50 GMT  
		Size: 91.5 KB (91528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0145c2a489ae7730d7223f460f80dafe51f0526dc47e623858fcde847197e00`  
		Last Modified: Sat, 26 Oct 2024 00:50:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d19f007f7ca8dec1ed3a8eded044546ad13d9929a677d9275175113c06a567`  
		Last Modified: Sat, 26 Oct 2024 00:50:50 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be329eeffb4ee6b33a67ff65486a2b854d413f95526ffc5c925d05e296ebbf3c`  
		Last Modified: Sat, 26 Oct 2024 00:50:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:0fc703c3774e2a62436b2e10f98e9e073d6c01d4a3a328869c48eb5a918b232b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **765.8 MB (765845566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510f31b7775f1b3875b215e531153cf95f04eadf5652b89072ac23cf82d567e3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 26 Oct 2024 00:49:36 GMT
SHELL [cmd /S /C]
# Sat, 26 Oct 2024 00:49:37 GMT
USER ContainerAdministrator
# Sat, 26 Oct 2024 00:49:51 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 26 Oct 2024 00:49:51 GMT
USER ContainerUser
# Sat, 26 Oct 2024 00:49:53 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 26 Oct 2024 00:49:53 GMT
ENV MONGO_VERSION=7.0.15
# Sat, 26 Oct 2024 00:50:40 GMT
COPY dir:420a97257b8f41b5187b8c509722525c37efef8c1a1591fc20aa57d257fef5d8 in C:\mongodb 
# Sat, 26 Oct 2024 00:50:46 GMT
RUN mongod --version
# Sat, 26 Oct 2024 00:50:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 26 Oct 2024 00:50:47 GMT
EXPOSE 27017
# Sat, 26 Oct 2024 00:50:48 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6295eceab893f6fea379800d4d13ef6f33bfa0076a1acecae1e4441cc1726578`  
		Last Modified: Sat, 26 Oct 2024 00:50:54 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7165801c732c7efaceb208a04ccb158a86d009f248fe4493737db5f9a4ce954`  
		Last Modified: Sat, 26 Oct 2024 00:50:54 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5079588087b813cb363d5ac1b1e604308abc5ebab5284ce9d1a2c2a7fa336ad7`  
		Last Modified: Sat, 26 Oct 2024 00:50:53 GMT  
		Size: 64.7 KB (64652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362bac848701833ed61ea1e02dcb2c8f340a11ca7b519a2018e73e23b7f44031`  
		Last Modified: Sat, 26 Oct 2024 00:50:53 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642cdc6a6b8ec95fbb4a20b390044d58096fe2466665f1e92a89e3273d937eb0`  
		Last Modified: Sat, 26 Oct 2024 00:50:53 GMT  
		Size: 275.1 KB (275148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94d0b411559a0fed7571a02794104eb4863c2468e4cc9dadbff9bf30fec3426`  
		Last Modified: Sat, 26 Oct 2024 00:50:53 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15058d47608772a2cd90ecdbd2a899751a49ad61787c037970ef51bd77902580`  
		Last Modified: Sat, 26 Oct 2024 00:51:40 GMT  
		Size: 610.3 MB (610337779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072bc211f48916731482e14e4e92e0c622ca4753fc4aa1026fb27a0e671d191b`  
		Last Modified: Sat, 26 Oct 2024 00:50:51 GMT  
		Size: 67.1 KB (67093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac11eaaa0691ec6968aa1101a907d0607b87e9c9c2048d1aecd92cacb44ac1c8`  
		Last Modified: Sat, 26 Oct 2024 00:50:51 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3086ceb0916a6e62229681c42569bb9771851cd48ee70957a5d662db890e8fdb`  
		Last Modified: Sat, 26 Oct 2024 00:50:51 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c1af4494fcdc4794cf476b8dfcc1fc2c64a3e178639d2ace747eb444c2ffdd`  
		Last Modified: Sat, 26 Oct 2024 00:50:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
