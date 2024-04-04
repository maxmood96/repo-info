## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:25cec4c0ad226fac44b5671965de236d30628f0daca1fbbe077739bbc99ded8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:5623c8cd57549465794442099ddda3237e5043a6d21af96128dcef4bae2d6f5f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **737.7 MB (737738254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03aeb1dbeff2ca6d339280b1f1b54c4aba8c334bdeddf5cdb6fc430bdd0dca40`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 03 Apr 2024 21:51:10 GMT
SHELL [cmd /S /C]
# Wed, 03 Apr 2024 21:51:11 GMT
USER ContainerAdministrator
# Wed, 03 Apr 2024 21:51:33 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 03 Apr 2024 21:51:33 GMT
USER ContainerUser
# Wed, 03 Apr 2024 21:51:35 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 03 Apr 2024 21:51:35 GMT
ENV MONGO_VERSION=7.0.8
# Wed, 03 Apr 2024 21:52:01 GMT
COPY dir:4a345f3390b35b1b56d808fec53236340ce99accef71314ef04d72a18e5c5b17 in C:\mongodb 
# Wed, 03 Apr 2024 21:52:17 GMT
RUN mongod --version
# Wed, 03 Apr 2024 21:52:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 03 Apr 2024 21:52:18 GMT
EXPOSE 27017
# Wed, 03 Apr 2024 21:52:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c31f05dd83a365212e3eccdf7ed24ebb4638fb1e7f92f723265ba10d0f184e`  
		Last Modified: Wed, 03 Apr 2024 21:52:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815d60597321cada9cae7fbcdcc095e40a5066f595cf8a921b0187f62bf7500c`  
		Last Modified: Wed, 03 Apr 2024 21:52:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cee37cc6b58254f8a063c35b343533f1f89d34e106d81eddc85d4b259c36132`  
		Last Modified: Wed, 03 Apr 2024 21:52:23 GMT  
		Size: 89.2 KB (89189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f39236ef75d06b6459750453d8578b65ace5ddb87e069f61aeb537855a3a1fa`  
		Last Modified: Wed, 03 Apr 2024 21:52:22 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2048fb10020a27ba5757f47377cec817ac6ab31877249f08fca4df6273c4a0c2`  
		Last Modified: Wed, 03 Apr 2024 21:52:22 GMT  
		Size: 267.1 KB (267085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f47a3d17eccbd5552c956ec67d51a524e5a66860ec477f3024b266244a1526`  
		Last Modified: Wed, 03 Apr 2024 21:52:22 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f6e046fca144ea754e28a33bf5a3cf529210e1ce621d45c093fe09dc5b5a43`  
		Last Modified: Wed, 03 Apr 2024 21:53:11 GMT  
		Size: 616.6 MB (616579556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780bf9339304b284d6de9165a27ec1de9a6315a46c21e54655fe25833e8d2f9a`  
		Last Modified: Wed, 03 Apr 2024 21:52:21 GMT  
		Size: 92.4 KB (92435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f36e7f9329dda1717c86f2a6229e3a08d216c12ed4236b332fabe191e47056`  
		Last Modified: Wed, 03 Apr 2024 21:52:21 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57b64b0384fc9f35c6578a936c52a9977bd5923d55c07b3335beaa80bca8ae8`  
		Last Modified: Wed, 03 Apr 2024 21:52:21 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362343bb756c9f2daf8b30328ae20fdf90cf7c4a6e46861f5d702222bb3f54ba`  
		Last Modified: Wed, 03 Apr 2024 21:52:21 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull mongo@sha256:1e3f20022a6de7a4d92a2fbdc4cc40eac645f804f961fe14777d997092030cee
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.8 MB (722841420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0006323c6f3d7ce6b3c91eb7396189666aa17f525526413944a54477fd74bdb1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 03 Apr 2024 21:50:41 GMT
SHELL [cmd /S /C]
# Wed, 03 Apr 2024 21:50:42 GMT
USER ContainerAdministrator
# Wed, 03 Apr 2024 21:50:51 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 03 Apr 2024 21:50:51 GMT
USER ContainerUser
# Wed, 03 Apr 2024 21:50:52 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 03 Apr 2024 21:50:53 GMT
ENV MONGO_VERSION=7.0.8
# Wed, 03 Apr 2024 21:51:35 GMT
COPY dir:4a345f3390b35b1b56d808fec53236340ce99accef71314ef04d72a18e5c5b17 in C:\mongodb 
# Wed, 03 Apr 2024 21:51:44 GMT
RUN mongod --version
# Wed, 03 Apr 2024 21:51:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 03 Apr 2024 21:51:45 GMT
EXPOSE 27017
# Wed, 03 Apr 2024 21:51:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19ead8e39e81fb8fde8b6712408021e6f380b735257aa0bc39f85a759b28c29`  
		Last Modified: Wed, 03 Apr 2024 21:51:54 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176c3a5738c8fd431c6feeaae5369526516e1dff3c16a382a7cb442b94b1e378`  
		Last Modified: Wed, 03 Apr 2024 21:51:54 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276b02947996a70053f37f806bb8fcd78865175590eccfee3844b88b7cfb94fb`  
		Last Modified: Wed, 03 Apr 2024 21:51:53 GMT  
		Size: 65.7 KB (65723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63eaa9cb002740cecdf0e719452ebe5f1a004ff2e6f08550e7e15f3795dd4080`  
		Last Modified: Wed, 03 Apr 2024 21:51:52 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b43ce700aeaf21c4d48ea5ce401dd29be9890b600073ca38befed373f93afbd`  
		Last Modified: Wed, 03 Apr 2024 21:51:52 GMT  
		Size: 267.1 KB (267052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f68d432158930f4bd2ffd135a7361742e5279279d149e8d10906e72ca6682c6`  
		Last Modified: Wed, 03 Apr 2024 21:51:51 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30073ceb975bdfc8b3a66bc0c6f9316baa091406508e63f1b420a2a33668d4bb`  
		Last Modified: Wed, 03 Apr 2024 21:52:40 GMT  
		Size: 616.6 MB (616579494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0e822557a119a4a18908342636496cbc75697bf3d2ad8c58fc7e555c5cae45`  
		Last Modified: Wed, 03 Apr 2024 21:51:51 GMT  
		Size: 1.3 MB (1301747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc049d4756acf9956e35d8ecd0750974b77000377b482e3152fab1e64bf048b3`  
		Last Modified: Wed, 03 Apr 2024 21:51:50 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31f352e0282b05eb2061981f7bc20a6deebdb67cb8d0243338c0b3e9fce371`  
		Last Modified: Wed, 03 Apr 2024 21:51:50 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726b1f3a26e76f1e05161d141a52aef4fe058eefd801624aceb23c4cae72348`  
		Last Modified: Wed, 03 Apr 2024 21:51:50 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
