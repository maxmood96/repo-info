## `mongo:4-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:7d08ac756b3417ccfcacde8d0c18d7acfea9367fb0ec27de40e563cd9cfaf03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `mongo:4-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

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
