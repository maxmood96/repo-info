## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:36171cb1896a4076f3ea7ba1732cbb0b4401c188bb1c3a6b242672f0a4bcdb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1970; amd64
	-	windows version 10.0.17763.4851; amd64

### `mongo:nanoserver` - windows version 10.0.20348.1970; amd64

```console
$ docker pull mongo@sha256:89bf3a5e03e6caaee41a7795efca6ca22ca111d91d50b0a5be61e38058c90607
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731091688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db526497a26c6d56687dcfd1e32b8c9bc29f0c2ec32b76fef52e24c096e5f545`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 01 Sep 2023 00:20:14 GMT
RUN Apply image 10.0.20348.1970
# Wed, 13 Sep 2023 01:45:13 GMT
SHELL [cmd /S /C]
# Wed, 13 Sep 2023 04:00:25 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 04:00:30 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Sep 2023 04:00:31 GMT
USER ContainerUser
# Wed, 13 Sep 2023 04:00:32 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Tue, 03 Oct 2023 01:22:24 GMT
ENV MONGO_VERSION=7.0.2
# Tue, 03 Oct 2023 01:23:13 GMT
COPY dir:966ad16c981f6f8ba3ff3658fdecd39e439aaa39e251615778ccd8944fcbfd3e in C:\mongodb 
# Tue, 03 Oct 2023 01:23:23 GMT
RUN mongod --version
# Tue, 03 Oct 2023 01:23:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 03 Oct 2023 01:23:25 GMT
EXPOSE 27017
# Tue, 03 Oct 2023 01:23:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8f8cef0759210af9d01a2fb45d79956a2db738bbd3734b7244b17e14ad945cab`  
		Last Modified: Tue, 12 Sep 2023 18:47:39 GMT  
		Size: 120.6 MB (120567584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c795bb9d48e9fa247e549604525fcb2599507cf1008aa1df12036f428ea236d`  
		Last Modified: Wed, 13 Sep 2023 02:18:07 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4d4f6211677cf82e6ed0d87f108ca902b6953cac7069b26a23966ebb167924`  
		Last Modified: Wed, 13 Sep 2023 04:38:18 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409b27824df1096550781d8d27fdafeb1abf5437c93f4d7bce18fdab09d1a67c`  
		Last Modified: Wed, 13 Sep 2023 04:38:16 GMT  
		Size: 79.5 KB (79488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01ed47b78f8c73c7cb1a91613a90350ec6f08cbad9f792825e0a51f4f144fd0`  
		Last Modified: Wed, 13 Sep 2023 04:38:16 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da139f5b1fbe899c90d6c3ef4302993f201f1ed8f81037e8c9b6dcfec78848ec`  
		Last Modified: Wed, 13 Sep 2023 04:38:16 GMT  
		Size: 267.2 KB (267173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6783b7937d1aea247bde5cbc1cf3e4c933e2ecb1c37fbde55f441cf5c54fd8`  
		Last Modified: Tue, 03 Oct 2023 02:26:28 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1dd38e2d572a3bc902da8e5f9a5617ed02959fe6da12ea68bc96b31926f827`  
		Last Modified: Tue, 03 Oct 2023 02:27:57 GMT  
		Size: 610.1 MB (610116889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218621a2fa7f25c490068cdea07316779a7eaaba18199773bad20db81bbca474`  
		Last Modified: Tue, 03 Oct 2023 02:26:26 GMT  
		Size: 52.4 KB (52420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46db93eafa9f283ab5f801bc0f2a32f503c1a1b9b873e5240ad4359994922380`  
		Last Modified: Tue, 03 Oct 2023 02:26:26 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cd9c29f8a2ebca2677030f14c1501d9ef23dd028d56a02cd49bbe789d14295`  
		Last Modified: Tue, 03 Oct 2023 02:26:26 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9393c1223a52c374c1a2804c2ada3c4910df70729a79000d011cc1c6f0bfd853`  
		Last Modified: Tue, 03 Oct 2023 02:26:26 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull mongo@sha256:7b6e344ae3beb70c4ca4ee0ecfd7eedca32db6b34f404f6b83a3d93dc2e48632
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.0 MB (715004771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f1c91fe2e5af5de03da6aa4a04045121943ca6c03bced5b2228d5b4b0a2e2b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 01:47:57 GMT
SHELL [cmd /S /C]
# Wed, 13 Sep 2023 04:01:38 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 04:01:43 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Sep 2023 04:01:44 GMT
USER ContainerUser
# Wed, 13 Sep 2023 04:01:45 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Tue, 03 Oct 2023 01:23:38 GMT
ENV MONGO_VERSION=7.0.2
# Tue, 03 Oct 2023 01:24:26 GMT
COPY dir:966ad16c981f6f8ba3ff3658fdecd39e439aaa39e251615778ccd8944fcbfd3e in C:\mongodb 
# Tue, 03 Oct 2023 01:24:39 GMT
RUN mongod --version
# Tue, 03 Oct 2023 01:24:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 03 Oct 2023 01:24:41 GMT
EXPOSE 27017
# Tue, 03 Oct 2023 01:24:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bbcbc05a0b3c240fc185ae93c7d844ad01c0d60ef9429ad4d230a78065a9ce`  
		Last Modified: Wed, 13 Sep 2023 02:18:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8461d082f0027d9ed1cd74ee8e9e1dbcb1250ea330332f1459c3a74a59e242`  
		Last Modified: Wed, 13 Sep 2023 04:39:52 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d24e4e27b8237cb6af207bc6c651cf8397fd4f0bd0e14d7fea42327ea04aa6`  
		Last Modified: Wed, 13 Sep 2023 04:39:51 GMT  
		Size: 70.2 KB (70185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0a145cf1519e52c048521ae1f199df2b6cba60425d6ed0fda7071a4785269e`  
		Last Modified: Wed, 13 Sep 2023 04:39:51 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482213ad81ac324a084b76c2ce668699bea68dea46dafa1de09c42aac5b042ed`  
		Last Modified: Wed, 13 Sep 2023 04:39:51 GMT  
		Size: 267.1 KB (267051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7fdddb9395665f3d0ee11b345c8de88ff5c2a9fedcbae28b1c693640d66ff6`  
		Last Modified: Tue, 03 Oct 2023 02:28:14 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cb627c12d57cf20aea8a341d4520a1251735bebe3a192e7df297847e4cc229`  
		Last Modified: Tue, 03 Oct 2023 02:29:42 GMT  
		Size: 610.1 MB (610116914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcac7d3333d34cb7d57a0b289e45d92a5a0c5bd6b24f21acb6638e28e0f62cd2`  
		Last Modified: Tue, 03 Oct 2023 02:28:13 GMT  
		Size: 50.3 KB (50266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23df4deef74156e7fc49be3ab6e2598cc42afe230ee7d6036b319e654c07e91`  
		Last Modified: Tue, 03 Oct 2023 02:28:13 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ab7469abcb7bb53a8443e28e11bd6047a8a49463d4a2c63d34f792c5b044d0`  
		Last Modified: Tue, 03 Oct 2023 02:28:13 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad909ec09a05893d6ac6b03366c0f1cb338f31b31bffd3c9cc8d62fa8bb819d3`  
		Last Modified: Tue, 03 Oct 2023 02:28:13 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
