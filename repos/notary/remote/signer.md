## `notary:signer`

```console
$ docker pull notary@sha256:39f01a2f9d9cb9112379d5b8c5a43319bf59a61f5979e55d9c78222640fff4e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `notary:signer` - linux; amd64

```console
$ docker pull notary@sha256:165564fed4dbab1f9af061dd035b7bf19a0baaab6ad3edf007308568f42aedab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33571db743a8f61899c12e66c37a30322154e4145289714e2f17521292f04528`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598998d406def7e37a6b047aafede720f173afae1e7d0c9d8754532edced1cc7`  
		Last Modified: Fri, 15 Mar 2024 23:55:41 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4c93ca41732c420131291f24ea955f0214502a2f226dd34db6be76c68a8817`  
		Last Modified: Fri, 15 Mar 2024 23:55:41 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8431174a1e366a5d57c8cf3cdfa51e53389f81abe8f3f2f86c677bce39e4521a`  
		Last Modified: Fri, 15 Mar 2024 23:55:41 GMT  
		Size: 4.8 MB (4763104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7831ea774cdf32dcdf25e00c82f5e4affb01d88cd6f3ca8e0c4ab12a772efbd`  
		Last Modified: Fri, 15 Mar 2024 23:55:41 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0696da5e464a807f3bd0467578a2b1a9965ffebe8a81c74a3db316c0f641f7`  
		Last Modified: Fri, 15 Mar 2024 23:55:42 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:f5590e975b15f1564dc37a8fb23ac835a0d0442e373583c08117190263f38f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 KB (123319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f541c609660b2af30e0484c229077d7dee4876d93fdb702a585b411fe78936fb`

```dockerfile
# Mon, 01 Jan 2001 00:00:00 GMT
RUN 
# Mon, 01 Jan 2001 00:00:00 GMT
RUN 
```

-	Layers:
	-	`sha256:bba906eac447b254388044e25a46082c06582e319329cd9307b763ea4f7deb06`  
		Last Modified: Fri, 15 Mar 2024 23:55:41 GMT  
		Size: 96.7 KB (96709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70de639185ba17522c49753aa565f10f4c655ffd4c7e520f49aba50ace51e62d`  
		Last Modified: Fri, 15 Mar 2024 23:55:41 GMT  
		Size: 19.2 KB (19244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c34aca72d8ab1446e2afeee6cebd46983df63996e477cf16ae7ea4b2e3bb0b40`  
		Last Modified: Fri, 15 Mar 2024 23:55:41 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.descriptor.v1+json+dsse
	-	`sha256:7c409924f1fc3a534ac26d681d468ffa6db137b4a41a7f32dad261d228a12d9e`  
		Last Modified: Fri, 15 Mar 2024 23:55:41 GMT  
		Size: 3.8 KB (3756 bytes)  
		MIME: application/vnd.oci.descriptor.v1+json+dsse

### `notary:signer` - linux; arm variant v6

```console
$ docker pull notary@sha256:aeaebe6db1cb96d37f70a2fead0b67392ba45976d81e7b2960f9ae386c1ff60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707b5a55c925b32e171ec8180da7559982e75199866fc624886353b0c8068b65`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74657dd1e96df2c28f1594d3eada4cc7e83a21c56c0523cb474fccd867dab4`  
		Last Modified: Tue, 30 Jan 2024 18:57:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec5e0de0f41694c6ad3e7e51c4169271f7ed41164469eb2c58e3016f3df5a76`  
		Last Modified: Tue, 30 Jan 2024 18:57:30 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45013e3a8f272dedb2d12cd13a6ae2c4d7e4b8954b331959e8b7697e334f691b`  
		Last Modified: Tue, 30 Jan 2024 18:57:31 GMT  
		Size: 4.5 MB (4526085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3497332bdba601b361bbc21d6a5f80bcd48d80bf093623867bcf738985c32615`  
		Last Modified: Tue, 30 Jan 2024 18:57:31 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c382fb4ce798e366082f207e7e1c7dad0e1d3542e556f09db7573909f0962018`  
		Last Modified: Tue, 30 Jan 2024 18:57:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:1191650cd9fcd22e23d16ffae6f4e318924dec99403d74e89ee24a09ddf18be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2943c57d34ac80a49eb5694f30352474c1613b729c440597bd8de013bb1d997f`

```dockerfile
```

-	Layers:
	-	`sha256:3bd2e6a70074f99ce6e977f4c3d67794009a984ab89dd45bb07d4769547b14a2`  
		Last Modified: Tue, 30 Jan 2024 18:57:31 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:56ba4141049fb7738bd7ffd13473df498ffa7a9ba62d77f3c35cc3c3cf765bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7103400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0839084c88f950d34fcd5df9ec723402893ba5dba5759bd4dfa2bf0ac8cc06bf`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9871114d42287b33918110eb07523b39cc14160b33769f724b170bf43a4c2448`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410538de933de15c8c872feb53b039d5090f04cbf7b5b48d31eb21346d92e79c`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3e6d0e154f38d04ff97de22e704ad8537b2d9f887a891c6a1813b2f201f636`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 4.4 MB (4393060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f28dbc4802c0caa3218e8a055b2df79716e0041a7fa925080e9dbc2167e8bb1`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b158b91aa8241285578eff6545cb4043ae4db56453ddbc63513f977d76b8d4ea`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:bf57fde03d0a04eb0304cedb3cef170a8083bac8990afaac825ac5ff221eb107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 KB (106482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37552696de213681e3034666073a74f3c72e726920def6452577ad6899cb164d`

```dockerfile
```

-	Layers:
	-	`sha256:b3c23b87aed798ef74162e46fb233939993124e6dd895d7dbfe326c38e3c706a`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 88.1 KB (88051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1fccc4d2d43a85912ff4b9d9422eb3afc680fda9050e4258c629f89f5b957fb`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; 386

```console
$ docker pull notary@sha256:685010a57a072d952934a2db41677cee2260573dbadd7e881c6f72cdacfc8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1a9ae4c671ae5ce1a64165ff4366aee62da61dbc9f4f89cea110021e7f967c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:d774e70db794cae73351fd822d82d497ead52871ac6abc00892b9d5df8d14ee9 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:f7286662823688d15d8d154fce6a97114514723ec2d9806a9527337308bd4dd9`  
		Last Modified: Sat, 27 Jan 2024 00:39:18 GMT  
		Size: 2.8 MB (2811055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e23a9a4d3fd14eb612e5eda8418b001357a5e223cd1e1f685ba0f13076defc9`  
		Last Modified: Fri, 15 Mar 2024 23:55:48 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bfcc25e8383ed9a421dd26f08ddc845a3f1838a0b8930430a115eb8a7ec40`  
		Last Modified: Fri, 15 Mar 2024 23:55:47 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f89f4d0aed5c3665e8a5fca43b28aad8c6c93ceda27376b8b6f73eb8107904a`  
		Last Modified: Fri, 15 Mar 2024 23:55:47 GMT  
		Size: 4.6 MB (4579023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c4c5122be26e9fd004c033c6c1e852b0a57c70afb13d84cf110c580a15c1fe`  
		Last Modified: Fri, 15 Mar 2024 23:55:47 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177c1c7d764a0fd565a38c4aa984a41645c709b1f5237396d8a395af77b79568`  
		Last Modified: Fri, 15 Mar 2024 23:55:48 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:24c5c3973f29dfedc157e12269a0b2a3d297389894ab323789964310b2a1212a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 KB (115911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84df828130669124ecf1ad1fa93c596d3adbfc640106bbf30f2a277e401097b`

```dockerfile
```

-	Layers:
	-	`sha256:4a96037ac7497fa5d4fccedca3d635596e6e0a3d8c4ee23c0c2b1fd5862cd25a`  
		Last Modified: Fri, 15 Mar 2024 23:55:47 GMT  
		Size: 96.7 KB (96694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8582114fb7963c945f73ad27abe5b05a79fd4a3cb65adfa1b59acdf5a4f57cfa`  
		Last Modified: Fri, 15 Mar 2024 23:55:47 GMT  
		Size: 19.2 KB (19217 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; ppc64le

```console
$ docker pull notary@sha256:2aa671033b8c981677f54a1a955816ba17022e29ea34c731dd928727efe41435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7102014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b934ca82675bc242409ce3effe5c3c870da59797b4795c5701de982cb9ff04c3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3351f370bc5e3633a2723c87d25ba725aa8a0e2029de4b1debe3a2cb508bec7`  
		Last Modified: Sat, 27 Jan 2024 09:53:58 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1599e40fe1c3eca2e8c8844e5ed20f33c0a09c663ff81b83c6ef38da62b0ea`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19113c8f1ecb888365a3790f47cf4aebb8550741024e85c140ef89ad0570933c`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 4.3 MB (4296967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a98e854f1812325b83d5185f2f0b01a4d4031b3cfa3cb0296613d11efbae3d`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a911ecfbc006e1f60d8125ac6058606d7337ae72554f858f5db12b013e49f233`  
		Last Modified: Sat, 27 Jan 2024 10:09:57 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:18a4a001219effc407e78bb00ad50daad58054be5bf87647728ac6dcbb73b58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 KB (104890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84d59bbfb301f09d4ceb96cfd4514c25aa6c7c051422d613013b9d51c8683b1`

```dockerfile
```

-	Layers:
	-	`sha256:f30b86170a1c97e33bb2c854853e600912733d0f8c124c2f69c0a2b41f16f0f3`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 86.4 KB (86430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e856cc9774a9ed314b963658cac098d54ca2ff2845415dc5f290f6e983c921`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 18.5 KB (18460 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; s390x

```console
$ docker pull notary@sha256:948a1e492bf8a8acfb50ab469d196def8e9c0067b6ba6638be96fcf5e8be38c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b013bf38fa165b3a0efcb803352b6dba52a1dc46b6d49ac5e12c1216e5c124`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b9d7ac5ec01e1212e2bab28ec95c28e4f9705a2c0d0b65a2d381dd75da59f65a in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:a7f1ea9eab1fb2b4aeff039474a8ee96afa63468cf85726a63ed8c31e861476d`  
		Last Modified: Sat, 27 Jan 2024 00:43:40 GMT  
		Size: 2.6 MB (2592124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2e4fcd23a75ab498c139f1a2a88ec5200c49da4be978f6b30a8f1c5509d8c5`  
		Last Modified: Sun, 28 Jan 2024 10:21:17 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b6dc6776403949de2056b9a44f45d62a49667d6e251c13d5358c5cf5df82b0`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd43f00868ac9c01f84b005bf43517b633cf861aef36c373b386b5411de4108`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 4.6 MB (4606699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb6ab9d90cdcc590780240eec3758ec407de20dbee201426247711decdf96be`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a56d00e6d9c7e85947fd8406dd9d17f21b08e532fd66a4a3619133f8b82c1a9`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:14ea2782ef369e9f938009c6758894f4265348da6f5e3e2ac39318d073c046d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 KB (104833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de48d74efbafdf2d12e2da9c741a467fd5bdeb2728c60940c8e0d38bf1048f56`

```dockerfile
```

-	Layers:
	-	`sha256:517239ce0f7e70d4ab9559e95222a78793405d8ce1bd1a2af0a18877996d9961`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 86.4 KB (86408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d3a1811181c41623a54c1a89a7b883647dd0c8f3a8fb65e0f99b37441dfff05`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json
