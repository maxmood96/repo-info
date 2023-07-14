## `mongo:5-nanoserver`

```console
$ docker pull mongo@sha256:93b5ff06e81240c57363e853ce45fa9d04976fc3dfb8725e879e973fbf57a7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `mongo:5-nanoserver` - windows version 10.0.20348.1850; amd64

```console
$ docker pull mongo@sha256:3101497adf1d6988beaed0111b1b26201cce809e91fefa93be841851ca54aac8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.4 MB (433364387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb186e0cafdd48ebc5dc09bb4c493abf7d4466a2d019f040941bbecdec4fb73`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jul 2023 21:00:40 GMT
RUN Apply image 10.0.20348.1850
# Thu, 13 Jul 2023 20:38:35 GMT
SHELL [cmd /S /C]
# Thu, 13 Jul 2023 22:41:28 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 22:41:38 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 13 Jul 2023 22:41:39 GMT
USER ContainerUser
# Thu, 13 Jul 2023 23:03:40 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Fri, 14 Jul 2023 04:23:04 GMT
ENV MONGO_VERSION=5.0.19
# Fri, 14 Jul 2023 04:23:29 GMT
COPY dir:6fc247d1b4a4949e8da3427789f654f844ec9ad3d9a0688e0d297b072e8b1b15 in C:\mongodb 
# Fri, 14 Jul 2023 04:23:44 GMT
RUN mongo --version && mongod --version
# Fri, 14 Jul 2023 04:23:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 14 Jul 2023 04:23:45 GMT
EXPOSE 27017
# Fri, 14 Jul 2023 04:23:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:cc0a26bd90fcc4d863317c36d7ffec77a0a82a905697204d4dcbc76ec13b3920`  
		Last Modified: Tue, 11 Jul 2023 20:10:45 GMT  
		Size: 120.1 MB (120056465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262f95c9ffc2400b306c39bdd21ab1ee5e02c305fa1895921355e39b04ef5049`  
		Last Modified: Thu, 13 Jul 2023 21:09:57 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c68dafb672cd72b022af598465e06fd23042d9e29348ccc200530e5b35d9bdf`  
		Last Modified: Thu, 13 Jul 2023 23:27:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1171b244f6f6515a32b709bf3ce287a50845db3a64ddc64026d75947c2af63`  
		Last Modified: Thu, 13 Jul 2023 23:27:01 GMT  
		Size: 80.2 KB (80237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943c2ea6e887132d6348c7c470e1eb8c8f31d8de00201b789ae3683c1d616638`  
		Last Modified: Thu, 13 Jul 2023 23:27:00 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ee32a4b650d1a8c59877c26864f499651e23cebe4c8258dd847dc3c8748ec3`  
		Last Modified: Thu, 13 Jul 2023 23:44:30 GMT  
		Size: 263.4 KB (263369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2353a5c982d18365db6289014cf4bc6c84ca4d6b30e22f1ada77354b4a4383`  
		Last Modified: Fri, 14 Jul 2023 04:46:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a97a65975887f7aaa42f240c9a746eeb7923404065a611b95b7c9a352a3374`  
		Last Modified: Fri, 14 Jul 2023 04:47:47 GMT  
		Size: 312.9 MB (312894420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bbc8a8cdf46eb5dd24a34b5a28cc7db882969f5d1b1461c723711643244098`  
		Last Modified: Fri, 14 Jul 2023 04:46:46 GMT  
		Size: 61.8 KB (61780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f8595a4f5287c78e341c5c89f79e7a172310b3453d549ec42e1aa70b942162`  
		Last Modified: Fri, 14 Jul 2023 04:46:45 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9a5e72fb81d698b3653735dcec8f05db5f77becd8668b83ac4b27095617bc4`  
		Last Modified: Fri, 14 Jul 2023 04:46:45 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9445332e31c8faabe20125f53c693a916cfc6d40ea6e047450354aec9c594cfc`  
		Last Modified: Fri, 14 Jul 2023 04:46:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull mongo@sha256:6f4af63c6b424dde699f3e82d121409d3d117d0ce93dd7a7afb2c33b34019452
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.7 MB (417716613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593a0b7d2b9ab688d6348e7ee022d5dea96a088531be5c5c2ff4b89ebc1cbe35`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 20:41:18 GMT
SHELL [cmd /S /C]
# Thu, 13 Jul 2023 22:42:56 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 22:43:04 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 13 Jul 2023 22:43:05 GMT
USER ContainerUser
# Thu, 13 Jul 2023 23:04:43 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Fri, 14 Jul 2023 04:23:57 GMT
ENV MONGO_VERSION=5.0.19
# Fri, 14 Jul 2023 04:24:22 GMT
COPY dir:6fc247d1b4a4949e8da3427789f654f844ec9ad3d9a0688e0d297b072e8b1b15 in C:\mongodb 
# Fri, 14 Jul 2023 04:24:33 GMT
RUN mongo --version && mongod --version
# Fri, 14 Jul 2023 04:24:34 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 14 Jul 2023 04:24:35 GMT
EXPOSE 27017
# Fri, 14 Jul 2023 04:24:36 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48271163dd58fddb2ff623ae3c53cac64a29148ad84e995c93073602f68793d`  
		Last Modified: Thu, 13 Jul 2023 21:10:35 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25653f1b79488d51860f4c39a7b5cb89dcde67e655debe7f7c2175ac330de2c`  
		Last Modified: Thu, 13 Jul 2023 23:28:43 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9847941203abbe97818feb1f724af0fd19021fcdc2b4bed652803609b6ee4a8`  
		Last Modified: Thu, 13 Jul 2023 23:28:41 GMT  
		Size: 68.8 KB (68839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257289d6eacacb75cbf84765b6355a008ee35bdf481b5b2b7989bbb19502ddb7`  
		Last Modified: Thu, 13 Jul 2023 23:28:41 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5546df12599902e639126688271cc1e2eedf2cb07fee83cfc7c18ac2bdb8bba`  
		Last Modified: Thu, 13 Jul 2023 23:45:35 GMT  
		Size: 263.5 KB (263502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa98a34faf73f62aa473be2010ece0470c840714918bec112027e4c28acbf13`  
		Last Modified: Fri, 14 Jul 2023 04:48:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae6f5c3bd2037675f7028fcaabaa76013cef666e5f0c21852f6e134ae1efbb7`  
		Last Modified: Fri, 14 Jul 2023 04:48:55 GMT  
		Size: 312.9 MB (312892580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84b2d062ef73496128d1aeda35e55ea9bea57dd740d9601906c67b16dbe9630`  
		Last Modified: Fri, 14 Jul 2023 04:48:00 GMT  
		Size: 75.4 KB (75399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdf5af2f47f7bdb38f3469653b9458091190a7861f3e5c4b35facee5cffd863`  
		Last Modified: Fri, 14 Jul 2023 04:48:00 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e884e4ee3a67137fb476932354c6a7e892f2750165f7bb4bbbffd413a6fb8005`  
		Last Modified: Fri, 14 Jul 2023 04:48:01 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a31e4b27b9ddcd5dc134077df82aebefda5a648b7c89320615ae7da3222c32a`  
		Last Modified: Fri, 14 Jul 2023 04:48:00 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
