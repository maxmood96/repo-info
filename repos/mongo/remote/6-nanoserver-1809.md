## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:e16a02fc56d21004e6a4a7977ac66f0ccbd687c9f58ca9e90901194a7288d59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull mongo@sha256:8df7ed2284e520876765a555c7a9846630daafc122936ecda3824c65ad7a3907
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.6 MB (681623392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7410d297a34e6fd22b011e6117f8a2b77cc4c1a7c154dd579e6fbb7f162045c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Thu, 16 Jan 2025 18:33:54 GMT
SHELL [cmd /S /C]
# Thu, 16 Jan 2025 18:33:55 GMT
USER ContainerAdministrator
# Thu, 16 Jan 2025 18:33:57 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 16 Jan 2025 18:33:58 GMT
USER ContainerUser
# Thu, 16 Jan 2025 18:33:59 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 16 Jan 2025 18:33:59 GMT
ENV MONGO_VERSION=6.0.20
# Thu, 16 Jan 2025 18:34:23 GMT
COPY dir:c42938a835e62388cb112585ef444a3c80db492841d999b4012ee48981a81e59 in C:\mongodb 
# Thu, 16 Jan 2025 18:34:30 GMT
RUN mongod --version
# Thu, 16 Jan 2025 18:34:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Jan 2025 18:34:32 GMT
EXPOSE 27017
# Thu, 16 Jan 2025 18:34:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950ad68a7a0348d71a06e68cc7d5c5cd0b511ba32375d5e8db63cfa646a3a1e2`  
		Last Modified: Thu, 16 Jan 2025 18:34:37 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1c1e01d0d3e93eae77e2eec9cb7d08a4f476b26c82a4d5163c74d706e2a534`  
		Last Modified: Thu, 16 Jan 2025 18:34:37 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07327ed495b9239b4c838a066cd691c0d63c6490523b2691d3220363d4636bcf`  
		Last Modified: Thu, 16 Jan 2025 18:34:36 GMT  
		Size: 74.6 KB (74563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ee6af897c35e075ab9dab2c5fc877aac8f60d60c03ba72d96d0c784c4f924`  
		Last Modified: Thu, 16 Jan 2025 18:34:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ed1bd022c2142d938711b86bda5778b80169be06f0aba726d9b821b78009dd`  
		Last Modified: Thu, 16 Jan 2025 18:34:36 GMT  
		Size: 275.1 KB (275150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e65d18c3f8066149f3c027dfa33ebcfb44c6612302a4e357fd6486655a4d829`  
		Last Modified: Thu, 16 Jan 2025 18:34:36 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40e06e91904990fb99585f0848eacadef7fa7ce0f3ffc8d94d27e11815dae49`  
		Last Modified: Thu, 16 Jan 2025 18:35:17 GMT  
		Size: 525.9 MB (525926902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e19c60f3e80fd1a230f37202582f1eddd7e1d027eb592d57e20356d4061ae`  
		Last Modified: Thu, 16 Jan 2025 18:34:35 GMT  
		Size: 71.8 KB (71827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780f10ba1db8a807f9e079d655414201533475d05d028ca409dde64feea445f8`  
		Last Modified: Thu, 16 Jan 2025 18:34:35 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd679d19aea1894261ca4b221ec1bce5f3b07e0ee8b4537baf5defe6f103390`  
		Last Modified: Thu, 16 Jan 2025 18:34:35 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52db786022f82d8dabd106d2f1bff7c390dbdd11f60d0b096a77cb86da32b83`  
		Last Modified: Thu, 16 Jan 2025 18:34:35 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
