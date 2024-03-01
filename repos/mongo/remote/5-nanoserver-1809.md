## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:e6f6554f8701581cdebfa8574d0784813e76008f8ee9cc7476aa5982c5897393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull mongo@sha256:952d83eb609f1ed1065b8a2314b728babd9b31d096a9e899e15ff7a933668969
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.9 MB (419945749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bc71944f13f4c3edb1567ee5bdb045fe2182162974d2053faad72b68a7ec37`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Fri, 01 Mar 2024 01:50:29 GMT
SHELL [cmd /S /C]
# Fri, 01 Mar 2024 01:50:32 GMT
USER ContainerAdministrator
# Fri, 01 Mar 2024 01:50:49 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 01 Mar 2024 01:50:49 GMT
USER ContainerUser
# Fri, 01 Mar 2024 01:50:51 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Fri, 01 Mar 2024 01:50:52 GMT
ENV MONGO_VERSION=5.0.25
# Fri, 01 Mar 2024 01:51:06 GMT
COPY dir:95d30a603d2e71c517181ebf96eae248a855a0fc4e8e1503c7f181fcfaf159de in C:\mongodb 
# Fri, 01 Mar 2024 01:51:18 GMT
RUN mongo --version && mongod --version
# Fri, 01 Mar 2024 01:51:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 01 Mar 2024 01:51:20 GMT
EXPOSE 27017
# Fri, 01 Mar 2024 01:51:21 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e137048cb3d84a3155cf3baa600c2074c55a73392b0eddd8da37b10bd686d2d`  
		Last Modified: Fri, 01 Mar 2024 01:51:26 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e4817fc350af0e045e9895e7960e606d13b0fca62365628d53d27cbb83b456`  
		Last Modified: Fri, 01 Mar 2024 01:51:26 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1601a64b505869dc1ff35936509d8362dda5efe6b436fe8fbdd1cbf16deff5`  
		Last Modified: Fri, 01 Mar 2024 01:51:25 GMT  
		Size: 68.1 KB (68051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d2f298eb753566dff96689653f3263762ed191fc10a2fc1d58b66c064049cb`  
		Last Modified: Fri, 01 Mar 2024 01:51:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ddb1538eb6c5c396d2747d9c4d64e772f92370f5f3b28f0f565faa54abd0399`  
		Last Modified: Fri, 01 Mar 2024 01:51:25 GMT  
		Size: 267.4 KB (267437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40f0445efe58963b558a61d9108fc42f8d22e929be89963ee504bf9ea25b171`  
		Last Modified: Fri, 01 Mar 2024 01:51:25 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b94624ba842c3ca479508d33009876a5af4677a3f1f22a82844f4c7f866e82e`  
		Last Modified: Fri, 01 Mar 2024 01:51:54 GMT  
		Size: 314.9 MB (314913640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b347859ebce8000684a6e7871609d9feff895af23b1a94b4f98b32795983f9f3`  
		Last Modified: Fri, 01 Mar 2024 01:51:24 GMT  
		Size: 67.7 KB (67735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff892d5681e5086bdf5867fdc6d43e91fa8adaea6a9978c15d5771addbb114cb`  
		Last Modified: Fri, 01 Mar 2024 01:51:24 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8522d663bb9ffb911b4f405177b4502333156e68cb2b2737dfb37cb4f340698e`  
		Last Modified: Fri, 01 Mar 2024 01:51:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5afdb518128f9ad97ac8afd4f39d4c15604a7ab7c230c73a354a8c1d81a005`  
		Last Modified: Fri, 01 Mar 2024 01:51:23 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
