## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:28c6246cbbc8280c7c1d50dfc49a80f5d8aee7b63608893e073c3304bdc1be2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull mongo@sha256:08cd8e9121c6fb07015cf97d2e584fcbe485ff8d28a8e69f73696e1accc68043
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351856442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba223eba4c9bd8b320bc925b9d2056175fb02bda326726120f7c458d32d5953`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:06:33 GMT
SHELL [cmd /S /C]
# Wed, 10 Apr 2024 01:06:35 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 01:06:37 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Apr 2024 01:06:38 GMT
USER ContainerUser
# Wed, 10 Apr 2024 01:06:40 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Wed, 10 Apr 2024 01:06:41 GMT
ENV MONGO_VERSION=4.4.29
# Wed, 10 Apr 2024 01:06:53 GMT
COPY dir:05c527a8cd901f69ca11856f2b42c60f8bfbb1c962d124799003a0c1b4353f7a in C:\mongodb 
# Wed, 10 Apr 2024 01:07:01 GMT
RUN mongo --version && mongod --version
# Wed, 10 Apr 2024 01:07:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Apr 2024 01:07:02 GMT
EXPOSE 27017
# Wed, 10 Apr 2024 01:07:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc69ae33384cc3255f74d3d4e8083efdd724a5b914fdd692fdbcb612179e5311`  
		Last Modified: Wed, 10 Apr 2024 01:07:08 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb335b60265e90f168b46f39c9c01828eceb7de44d2f0214f98c3b74d51ae029`  
		Last Modified: Wed, 10 Apr 2024 01:07:07 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864d07ce6bd5d32fd0ab9d9b5736e4077c9e1c20e3911451b92f57f5fece49ab`  
		Last Modified: Wed, 10 Apr 2024 01:07:07 GMT  
		Size: 72.5 KB (72492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48019f36ac58df8e137a757a061fea5e770a625037e5a12e858f98f9cee9e03`  
		Last Modified: Wed, 10 Apr 2024 01:07:06 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3782d586ac8023234eaea1a2163d95b63e4a25f23dc9561a449c8f0f5c0717`  
		Last Modified: Wed, 10 Apr 2024 01:07:06 GMT  
		Size: 267.4 KB (267434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e95c535ea799aab7215ba0e8a8f7219bde9beb3f519a56c0dc75e64f8c87c3`  
		Last Modified: Wed, 10 Apr 2024 01:07:06 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc43d2abcd69a2c789bac51ef54ed955c02487a8bc07059aaf4ac8c2b1c84e9`  
		Last Modified: Wed, 10 Apr 2024 01:07:30 GMT  
		Size: 245.3 MB (245305535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9810037ca884993a8dbbb3f1af72b3e21f22c13382a047cf2854688f98b33e3a`  
		Last Modified: Wed, 10 Apr 2024 01:07:05 GMT  
		Size: 1.3 MB (1314611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c97f7fc6a6d0af2edfe458081c32596b078dcdd468ac781b4489d9bc41a5257`  
		Last Modified: Wed, 10 Apr 2024 01:07:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8be34a98055425386e390e86e437337870079f27475b75ac07a2720c8187be`  
		Last Modified: Wed, 10 Apr 2024 01:07:05 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c418659d33802576f9f41e671d001d5f220ace16f8d11a279ba3dd99dbce6640`  
		Last Modified: Wed, 10 Apr 2024 01:07:05 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
