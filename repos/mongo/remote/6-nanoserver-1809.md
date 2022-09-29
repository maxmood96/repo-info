## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:19e6f5d2e5f7d67bae9f96c9ae63607ef9389257b389a26324fd47eae50307ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull mongo@sha256:b97e6091010668c1eaf425553c04a4f201b06e6c760330ed53a10fe2a2ef9804
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.1 MB (615114240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2391f80c327356ccf2611f5fbf8d8a82604b9466bde2cac5a29515755de0daa5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 13:03:35 GMT
SHELL [cmd /S /C]
# Wed, 14 Sep 2022 18:18:09 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 18:18:21 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 Sep 2022 18:18:22 GMT
USER ContainerUser
# Wed, 14 Sep 2022 18:18:23 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Thu, 29 Sep 2022 20:23:11 GMT
ENV MONGO_VERSION=6.0.2
# Thu, 29 Sep 2022 20:23:59 GMT
COPY dir:4123bc4d354fb6abb19af459f2430680f89ba0d88861da6bacc3b060f799c08d in C:\mongodb 
# Thu, 29 Sep 2022 20:24:14 GMT
RUN mongod --version
# Thu, 29 Sep 2022 20:24:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 29 Sep 2022 20:24:16 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 20:24:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0668477bacdfc2e7df1cd4268b246175ed9b30cf07ccb4bcfcb258d8bee830e`  
		Last Modified: Wed, 14 Sep 2022 13:26:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ada06039b3dceb53c91ed6d7bd2d77d0abd90acba1883744d947d1ccee8349`  
		Last Modified: Wed, 14 Sep 2022 19:03:38 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d170c6bf2fd2a53a952e69b17f97ce92dd39dd7294e4b1c6ae6e11adc613210`  
		Last Modified: Wed, 14 Sep 2022 19:03:36 GMT  
		Size: 69.7 KB (69673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d16b6830f5e893640af2e263523f5ff88334d46d1a2d69d91cddf1f70f62790`  
		Last Modified: Wed, 14 Sep 2022 19:03:36 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85506cad2fde8d32c24db2c875bf6985f88404029a892afe534fa01b72847539`  
		Last Modified: Wed, 14 Sep 2022 19:03:36 GMT  
		Size: 267.1 KB (267096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b809ee05395f7e65d727af42aa4cc79a32dcec0c60710d817a73ab4422d8d25`  
		Last Modified: Thu, 29 Sep 2022 20:45:29 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08d4885c748864b6ed5b55d734b6c33a85df5e2cebb8dd315fcaf3a3db9c2e4`  
		Last Modified: Thu, 29 Sep 2022 20:46:46 GMT  
		Size: 511.4 MB (511354304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76677c50b5ec51f292ea51d30cc95435cbbb29e873306ac0c08e243bdae28337`  
		Last Modified: Thu, 29 Sep 2022 20:45:27 GMT  
		Size: 81.1 KB (81072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9a6ece0447655211a82e6b4c73e298903006d1e6b6bb422e03f20b9c60405`  
		Last Modified: Thu, 29 Sep 2022 20:45:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f0ca8f1ff6163c7bcf9ef48fdadef6ce293e1dd796a065a9890391f2c736aa`  
		Last Modified: Thu, 29 Sep 2022 20:45:27 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26faf5e631c893abbbb30ccfff7ca3febba4f5326beae352d832ed4715e32728`  
		Last Modified: Thu, 29 Sep 2022 20:45:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
