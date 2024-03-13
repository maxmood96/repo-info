## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:05c29fe950c61bbcc96af15163fb8bcd6390df0e6bc3e7a192889c6e23dd21f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `mongo:nanoserver` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:5ca364dbd8c9712b5629362575b4c62de7c65753abdb2751eb1514025809bdd2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **735.0 MB (734993822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e572b22c9f09eeabc4d60f12ff0ccfe3d26a7946a6066263fac26757042937`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 02:05:50 GMT
SHELL [cmd /S /C]
# Wed, 13 Mar 2024 02:05:51 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 02:05:54 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Mar 2024 02:05:55 GMT
USER ContainerUser
# Wed, 13 Mar 2024 02:05:56 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 13 Mar 2024 02:05:57 GMT
ENV MONGO_VERSION=7.0.6
# Wed, 13 Mar 2024 02:06:24 GMT
COPY dir:760432e495467387aee1f5ff3c4832ced81799e4ea6e068f15089694b9856264 in C:\mongodb 
# Wed, 13 Mar 2024 02:06:41 GMT
RUN mongod --version
# Wed, 13 Mar 2024 02:06:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 02:06:42 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 02:06:43 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791d1b3101c80f832ab79cef86e54668bced56ff2e582a610d26db6f6628ae6e`  
		Last Modified: Wed, 13 Mar 2024 02:06:52 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3603a8aab79f196b33be996d1ad6a0b2d9949dfb72bbc6a1d52b7d37053d2704`  
		Last Modified: Wed, 13 Mar 2024 02:06:52 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc9d049948cbbde2b10d6c57f866f57b9f586da04f468f3f35413e99c9e4de8`  
		Last Modified: Wed, 13 Mar 2024 02:06:50 GMT  
		Size: 77.3 KB (77297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee1472b8a74e38a372dc4b0f917aa5b6ab16dd747cbc102ee9f98fb4253267d`  
		Last Modified: Wed, 13 Mar 2024 02:06:50 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc11c038bd398838b3f5e534bc47ae8d473fb4c482f4d221ce4708632ca7ddcf`  
		Last Modified: Wed, 13 Mar 2024 02:06:50 GMT  
		Size: 267.1 KB (267067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b174affdaf66dede7165c433ea950cb0fa06f022f2c2da514c9c0bfa8a5932ed`  
		Last Modified: Wed, 13 Mar 2024 02:06:50 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037298f043cb5a253b206ebac77f21ff83e1d9bd20c7efb92cedef7e283b78bd`  
		Last Modified: Wed, 13 Mar 2024 02:07:38 GMT  
		Size: 613.8 MB (613839345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816dbc35df5307942667f5e8d04faa84fe8007568be08518245ed332fde7b4ed`  
		Last Modified: Wed, 13 Mar 2024 02:06:48 GMT  
		Size: 100.1 KB (100131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1e51dd872791e08dfd4a809a2f84f4da6feeaa97e81324f238527cfeb32dcf`  
		Last Modified: Wed, 13 Mar 2024 02:06:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06ec578f6965bedee606b4b02b54149b1080eec8b3cef5895900b06b755f770`  
		Last Modified: Wed, 13 Mar 2024 02:06:47 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f99150592655469cae1066b5f56068846da65f245e7afd6555f175c383b888`  
		Last Modified: Wed, 13 Mar 2024 02:06:47 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull mongo@sha256:25ee097f50966cd642375feb13cb43c12895a74a8aac94390a12c579549731e7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.1 MB (720120181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc3948bbec7b66322d5a49775a18e2a266543f3911a8c3239bc9b4ea45429f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:10:52 GMT
SHELL [cmd /S /C]
# Wed, 13 Mar 2024 02:10:53 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 02:10:55 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Mar 2024 02:10:56 GMT
USER ContainerUser
# Wed, 13 Mar 2024 02:10:58 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 13 Mar 2024 02:10:58 GMT
ENV MONGO_VERSION=7.0.6
# Wed, 13 Mar 2024 02:11:35 GMT
COPY dir:760432e495467387aee1f5ff3c4832ced81799e4ea6e068f15089694b9856264 in C:\mongodb 
# Wed, 13 Mar 2024 02:11:45 GMT
RUN mongod --version
# Wed, 13 Mar 2024 02:11:46 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 02:11:47 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 02:11:47 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31908f28ff948e751fb5fd7e09eb76a61e3f8cc748cb0eeda142c2d8fb66dc7`  
		Last Modified: Wed, 13 Mar 2024 02:11:52 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd460b88c67a39cfcb30518402c90b2dd0cf7ca463c8f10d7e55531e53b86c9b`  
		Last Modified: Wed, 13 Mar 2024 02:11:52 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801574abad8e63d9112aa84b8321412061f88719a4d510eb6983ff2a85451ae5`  
		Last Modified: Wed, 13 Mar 2024 02:11:51 GMT  
		Size: 69.9 KB (69899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b4717eae3d40855cdfe18a55c38b8ec4d9d427cd8c5f465b9c84f51042cab`  
		Last Modified: Wed, 13 Mar 2024 02:11:51 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf851c2345c933a09b8d3aebb45ef405cbccc68f3c5cbc94a06a5d4b0031cca6`  
		Last Modified: Wed, 13 Mar 2024 02:11:51 GMT  
		Size: 267.0 KB (267048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a297bf9c7a1567cf8e0bb4d1ea9732e26a8d67642c66141c41a46896a073f18`  
		Last Modified: Wed, 13 Mar 2024 02:11:51 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ec70b1ba4d7b3c6fa186e8e8ce85d50322ea2fd9b1bb40067cefe5a5b9381b`  
		Last Modified: Wed, 13 Mar 2024 02:12:38 GMT  
		Size: 613.8 MB (613839274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314830d74930b72b4b937b4a54e311b858bb34a48906d7941270981e9ec902ed`  
		Last Modified: Wed, 13 Mar 2024 02:11:50 GMT  
		Size: 1.3 MB (1316597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0145e52f4c535e6cffc00645e502959156ce0fcabe57f6e726c075357a8f76`  
		Last Modified: Wed, 13 Mar 2024 02:11:49 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8623a3791c0f55c6c77334efe2cc86e6b59c35b68449e483c66d750ac705196e`  
		Last Modified: Wed, 13 Mar 2024 02:11:49 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4989ffc701e7b6247382c6db76bec728956eb9072c7cf6ef8b4c4d36b8c2e0b9`  
		Last Modified: Wed, 13 Mar 2024 02:11:49 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
