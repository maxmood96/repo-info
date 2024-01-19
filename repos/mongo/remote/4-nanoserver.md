## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:d0febcba05f09821d34a79ad0acc2d92fb976e709cf94e5aa34f1974e1c2f190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.2227; amd64

```console
$ docker pull mongo@sha256:34be50e29f2f0a4478219feba60b5fc8606c55235d326063720785001bd4fc3d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.8 MB (365814984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232ef013578866ed7478e2afd4b8f0e9e08a28317a0b854f69eac5a4fd3eb6c7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Fri, 19 Jan 2024 00:52:06 GMT
SHELL [cmd /S /C]
# Fri, 19 Jan 2024 00:52:07 GMT
USER ContainerAdministrator
# Fri, 19 Jan 2024 00:52:41 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 19 Jan 2024 00:52:42 GMT
USER ContainerUser
# Fri, 19 Jan 2024 00:52:46 GMT
COPY multi:d83167ee7f0a01f519841410f1f031c3bdfa566af08cc1936efaf3b3f20e2b0f in C:\Windows\System32\ 
# Fri, 19 Jan 2024 00:52:47 GMT
ENV MONGO_VERSION=4.4.28
# Fri, 19 Jan 2024 00:53:01 GMT
COPY dir:a7c7b908528d01fb9f70c066b06420934555f7d49e4fc1a503daaffbd0c2ab90 in C:\mongodb 
# Fri, 19 Jan 2024 00:53:11 GMT
RUN mongo --version && mongod --version
# Fri, 19 Jan 2024 00:53:11 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 19 Jan 2024 00:53:12 GMT
EXPOSE 27017
# Fri, 19 Jan 2024 00:53:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf96504d64ee3ae316bcc22a118441463e93c384aa50ccf1416a413af0f637a7`  
		Last Modified: Fri, 19 Jan 2024 00:53:22 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dd54b8ac5df85df3f2336babd9a987203cb9621a2140e71fb2154279b747d6`  
		Last Modified: Fri, 19 Jan 2024 00:53:22 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0a3df37408136af7dc8b564bd37c90864508aa698432c91c696b479964ae7c`  
		Last Modified: Fri, 19 Jan 2024 00:53:21 GMT  
		Size: 74.4 KB (74439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cbb561f888d176c50a6d3832deb1398c1be1a5818be4c422cf8974b409feb4`  
		Last Modified: Fri, 19 Jan 2024 00:53:19 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22175acb76cb29cb11e4ffc4342179ccdb98b0372091a1674846dfd0271eae2`  
		Last Modified: Fri, 19 Jan 2024 00:53:20 GMT  
		Size: 263.4 KB (263422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622853ccf549be909f1d2fae7505b5fc631b58c5066bc8085b4362667f729ac0`  
		Last Modified: Fri, 19 Jan 2024 00:53:19 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dc5167142cf43ae25acdcc60e50ffdd047900ed6e95f8c361087556fa59cf4`  
		Last Modified: Fri, 19 Jan 2024 00:53:41 GMT  
		Size: 244.6 MB (244614423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6fe7e875b5f9b23e13f1693589d09737a783961f9c3bb1130d49278ee02edf`  
		Last Modified: Fri, 19 Jan 2024 00:53:17 GMT  
		Size: 86.2 KB (86160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35c283e5e321ab5033fb54d86ffa4b08dbad55ad644138e5416fb97105f938e`  
		Last Modified: Fri, 19 Jan 2024 00:53:17 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a488a9f6d8f7c459c9b32a27bc941469999195fda03e86beb378138c6c2ccc`  
		Last Modified: Fri, 19 Jan 2024 00:53:17 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2237a2bab4041909b54176dc7dfde52a762f971d90aedbdc3ad12bb72004da31`  
		Last Modified: Fri, 19 Jan 2024 00:53:17 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull mongo@sha256:cc6694dd4c26ad6a84891d7bc9e6d213d15ab863140793428bb3e6e764823516
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349617093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adced889d7a1ec5586faa60d41fea3012c791aa3f021b6f7cdd71a7a20d97fa7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Fri, 19 Jan 2024 00:51:34 GMT
SHELL [cmd /S /C]
# Fri, 19 Jan 2024 00:51:35 GMT
USER ContainerAdministrator
# Fri, 19 Jan 2024 00:51:39 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 19 Jan 2024 00:51:40 GMT
USER ContainerUser
# Fri, 19 Jan 2024 00:51:41 GMT
COPY multi:d83167ee7f0a01f519841410f1f031c3bdfa566af08cc1936efaf3b3f20e2b0f in C:\Windows\System32\ 
# Fri, 19 Jan 2024 00:51:41 GMT
ENV MONGO_VERSION=4.4.28
# Fri, 19 Jan 2024 00:51:56 GMT
COPY dir:a7c7b908528d01fb9f70c066b06420934555f7d49e4fc1a503daaffbd0c2ab90 in C:\mongodb 
# Fri, 19 Jan 2024 00:52:02 GMT
RUN mongo --version && mongod --version
# Fri, 19 Jan 2024 00:52:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 19 Jan 2024 00:52:03 GMT
EXPOSE 27017
# Fri, 19 Jan 2024 00:52:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9161bfac4c420fdb686d0360d63f3945a6c353229e2b8be05d9f200cd2753c76`  
		Last Modified: Fri, 19 Jan 2024 00:52:12 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338dcc7a02ef6ce28e3c387c0beef60b8136f34e2c9ca6f4e1cb8a14acba8a1f`  
		Last Modified: Fri, 19 Jan 2024 00:52:11 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314c16ee78f534a13c24882c78aadb56e78d40bc1822d78fbc8cd8be787a6c0a`  
		Last Modified: Fri, 19 Jan 2024 00:52:10 GMT  
		Size: 69.0 KB (68979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5035a82426f1657d499006208f56a00c26c970ba97eaf0291611edad8f8a1c6`  
		Last Modified: Fri, 19 Jan 2024 00:52:10 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19898259eb8cf023d085b44a8e9210cef9700dade59260144186907153cb9b13`  
		Last Modified: Fri, 19 Jan 2024 00:52:11 GMT  
		Size: 263.4 KB (263435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5c1d0c401ee488445a4fc18f882ea628e9dea9c3e5dfe79bcc6476f6e28879`  
		Last Modified: Fri, 19 Jan 2024 00:52:10 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77b8138634499e3f25ffa337089a4af1fe589d15ef2a3a6901fb53f09af92d2`  
		Last Modified: Fri, 19 Jan 2024 00:52:32 GMT  
		Size: 244.6 MB (244614703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90fc68e71c63dc677783692c01b935543136c683d82d6b7303ca0648614833`  
		Last Modified: Fri, 19 Jan 2024 00:52:08 GMT  
		Size: 71.3 KB (71266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40be9a0c76912dbc4078348961ee980eb81c2bf42537ebf48fe1b512f0ef61f9`  
		Last Modified: Fri, 19 Jan 2024 00:52:08 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2963b66503843fa2c14f2a793b36d930ea1dd071d41599b6ed5f1b8a6a03fe0`  
		Last Modified: Fri, 19 Jan 2024 00:52:07 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935741dcd8693b03910a47e57278ab25a962237436080bef6ab87b23a2711e76`  
		Last Modified: Fri, 19 Jan 2024 00:52:08 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
