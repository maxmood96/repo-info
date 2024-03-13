## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:13e083712500f4b181372688fde18d88c1a91b5da90d12d052a79fea7a2ee6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull mongo@sha256:b74e608dc1ca7f29ce6454694851dcb801a615dbaead3e1e249c3df8ef5bd0b5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.2 MB (627176727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f971eed02df188284bf31b03c555e0819452d9ae60071d72778f92f8594972`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:07:04 GMT
SHELL [cmd /S /C]
# Wed, 13 Mar 2024 02:07:04 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 02:07:07 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Mar 2024 02:07:07 GMT
USER ContainerUser
# Wed, 13 Mar 2024 02:07:08 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 13 Mar 2024 02:07:09 GMT
ENV MONGO_VERSION=6.0.14
# Wed, 13 Mar 2024 02:07:46 GMT
COPY dir:254820e97691f1aa9249d91faf05efbef599ba0e97089379ceabe51f49c02c4a in C:\mongodb 
# Wed, 13 Mar 2024 02:07:56 GMT
RUN mongod --version
# Wed, 13 Mar 2024 02:07:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 02:07:57 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 02:07:58 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85a108a26f2d58bd0963ec127746672752259a3441a4d7da3ff411c848c532b`  
		Last Modified: Wed, 13 Mar 2024 02:08:07 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfd70d8d430e356aad2c0ad5578c62f6e745aaf377ddabfc53b4ba8e049dedf`  
		Last Modified: Wed, 13 Mar 2024 02:08:07 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebe90984448560754ad7b3096f35123aee54240cfa1f07311d34addd7053cba`  
		Last Modified: Wed, 13 Mar 2024 02:08:05 GMT  
		Size: 70.8 KB (70808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefd64d4c02e37bcdd61a0f6a8414e482f283c4578095d6cfe937817f3ef6a44`  
		Last Modified: Wed, 13 Mar 2024 02:08:05 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d696e2541d0df58ddc63493370794d309a58e0969d615a5b3007440072eb5a7a`  
		Last Modified: Wed, 13 Mar 2024 02:08:05 GMT  
		Size: 267.1 KB (267060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1406ef0ec9eab0c58677db38f8ec8ce75710e0549985bd64214572d0a1f08c3`  
		Last Modified: Wed, 13 Mar 2024 02:08:04 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092d0d1c61f2e9c1638916fc41a9056fbae214c3005a79660e6f0c6d9b2e078e`  
		Last Modified: Wed, 13 Mar 2024 02:08:46 GMT  
		Size: 520.9 MB (520890957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94fb32546a4d3adc8ad31ea195e06d86a169596a4593219bfbb6ad4dab1a80c`  
		Last Modified: Wed, 13 Mar 2024 02:08:03 GMT  
		Size: 1.3 MB (1320526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6470aaf94403f265c32daa58ddd0961a187c82d98081f60a662e69aba40818`  
		Last Modified: Wed, 13 Mar 2024 02:08:03 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc8f8f1bf02e13666606a71533cffe8d1d16a5e288898ad947a805468c70949`  
		Last Modified: Wed, 13 Mar 2024 02:08:03 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e85a068c234e556a4e0bbbabc6855bf664131a2006950937ce53e70601571a5`  
		Last Modified: Wed, 13 Mar 2024 02:08:02 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
