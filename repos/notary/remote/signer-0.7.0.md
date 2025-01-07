## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:62178bbf11d4418d02d8a41f9fd419e95d66e11c5b00909f8638e8673fc4cb00
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

### `notary:signer-0.7.0` - linux; amd64

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

### `notary:signer-0.7.0` - unknown; unknown

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

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:a76c22d2b6f9d44b8142a950da1cfba61445e22c70b7996d0d61831e621d017c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8117757b95b529ddb5aaa4ecb6d3c6c9d0ee51ac763fc12d19b61c09842dfee9`
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
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8ee0fe68961d6ee52c91239fdf2be6eda70ccd54aa2fd8a66ac8baad840022`  
		Last Modified: Mon, 18 Mar 2024 16:05:07 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4f6f7afa34ddfcb616d218ee580f9e325b2ce5e67c3808e7cf705e07c68e92`  
		Last Modified: Mon, 18 Mar 2024 16:05:24 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04661da5919a9936ad4c008a67eaeed0e35623ab3639c79f92471ed517696b61`  
		Last Modified: Mon, 18 Mar 2024 16:05:25 GMT  
		Size: 4.5 MB (4526083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e3963d1f6c0b84d902a10fd2436858a6c2ca352b7f9a11a900954c1c4f4c88`  
		Last Modified: Mon, 18 Mar 2024 16:05:24 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34589411af2e17d04d981d078bbe0a72fb854bec0188371246f576cffb3eb357`  
		Last Modified: Mon, 18 Mar 2024 16:05:24 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:7084382ea8fe4e275d83464987f65694b588507243a437b849032b5e6a2f665a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e723a18fbbafe10b84888e572dabcf296d0fc17a2a39c361140778ff050b8d8`

```dockerfile
```

-	Layers:
	-	`sha256:fb8b690f2731c2af045641eaab069d5ce871a2e9903ba745148ed33b795987ae`  
		Last Modified: Mon, 18 Mar 2024 16:05:24 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:ad768715eb36df81309a0d28768fcb01b91979ba5f373a7d543d64062056bfcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7103392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2add9ad749482dcbb83cdfa74039c0e35dcb8e719d797eb905951ba3608fad3a`
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
	-	`sha256:46cf874dd167e3be1f118079798127256ef5d5caafc2546040bb3cde47cf7e8c`  
		Last Modified: Sat, 16 Mar 2024 15:49:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5da7acd3d635e5ea2c96c6064ed1086b06552e9923339a537edf25fd2c9f41b`  
		Last Modified: Sat, 16 Mar 2024 15:49:31 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b16276b3e752da6d1f2323971d646cb9768612c4ae298a2f12c966176b7352`  
		Last Modified: Sat, 16 Mar 2024 15:49:31 GMT  
		Size: 4.4 MB (4393056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48871dc50336712f2ea46096b5ac284207fabaf89d71394bc322473f6580bd`  
		Last Modified: Sat, 16 Mar 2024 15:49:31 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f4499561d9a9119b7fedaf25ad55198f7c69ae9d926ddfd486d4338909734d`  
		Last Modified: Sat, 16 Mar 2024 15:49:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:00e453626795750671543855488e17d9b70f263458fa914e5466123a112a351c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2386b6fff955ef85ec5504095c9de8c88d7f1c0fbcd6b9765d571e1f9c345f`

```dockerfile
```

-	Layers:
	-	`sha256:8fd6d0681b9a5f70c04a29a10f6ae83fc92e39a967426153745551b916318ff2`  
		Last Modified: Sat, 16 Mar 2024 15:49:31 GMT  
		Size: 96.7 KB (96716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faa8d302ab055339f450fa910a0ce8af9da2efaf28eeb5106230956c91330504`  
		Last Modified: Sat, 16 Mar 2024 15:49:31 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; 386

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

### `notary:signer-0.7.0` - unknown; unknown

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

### `notary:signer-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:c7267174db52c3902aca7afd3802dabdb05eb8b759734e6544f4f0916f453f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7102040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e80b9f4ce79e1e52b4669e9d854e317c782e8c5ec3a8f098727add3fde03cd`
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
	-	`sha256:0bdd1c5d3e50adc22c43338f6229f0cb0a9078a2b9498124d390dc7ca3e57ea1`  
		Last Modified: Sat, 16 Mar 2024 10:33:53 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51799d14881395aab5523851d28cd4d38152ef2561449580e82c248830848bed`  
		Last Modified: Sat, 16 Mar 2024 10:34:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9a9bc9dbd03912dd05947826d7c8c1c2f4a649cc150e5d24e9093214430737`  
		Last Modified: Sat, 16 Mar 2024 10:34:19 GMT  
		Size: 4.3 MB (4296993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d6f88114303c019db74807ce120dedc88f0b82788c35b9dd3bbcfcef7b35df`  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bce13479dfad62d6689e970d72ac66774849a79e1b549ecd0c603e8d91cb59`  
		Last Modified: Sat, 16 Mar 2024 10:34:19 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:e0b80caef7399f7aa8a5695f0bdb3ca1ea0087b91fab189c4b45239e26f6fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0b3f786cef51ef4bcbd49b2f8a09c98aefc8cf653fe17ba44c9f97fe4ce91e`

```dockerfile
```

-	Layers:
	-	`sha256:b8b14edb273267c9b9963320d345eb985865c9b4cf889464916b61438e61e9eb`  
		Last Modified: Sat, 16 Mar 2024 10:34:19 GMT  
		Size: 94.8 KB (94777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42eb964a753f455e098519a381c4533d519aa5c789cd10f9cc17d5d7243874f`  
		Last Modified: Sat, 16 Mar 2024 10:34:19 GMT  
		Size: 18.5 KB (18461 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:17b88d327729e1a36eede7920e44ab0417d6637e6e292891aa0ac38a3963e1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa2695e4c713b26d64d9b27a817e0bfc96020e9d361fffeea667ac0fe039bda`
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
	-	`sha256:2d495ce178eb936d65241f75f3c49b1a8688ae60a9854465dfac55bd788186dd`  
		Last Modified: Sun, 17 Mar 2024 22:25:09 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56acc24b23285e0ab13f1b5b0fa9d582b8672b64d79249df493fc7cdeba2184`  
		Last Modified: Sun, 17 Mar 2024 22:28:18 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d1dd2c8a742575593ab89298778f4bbd21369c06d450882308bea8b597d2ad`  
		Last Modified: Sun, 17 Mar 2024 22:28:17 GMT  
		Size: 4.6 MB (4606701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1cfec39facefca23715d5b82cfef5f721b9ecd860050972694509ea984de5d`  
		Last Modified: Sun, 17 Mar 2024 22:28:17 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb7a9d68b80a529028bd07ff4aa947d73b306c43df57298e5309879545a8c04`  
		Last Modified: Sun, 17 Mar 2024 22:28:17 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:e8326eb34838897b53c80aaab771af4cc16c0298768228f8cc4ba82672a4e88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2c91e68d9d03604197ece2ce1a72e8260bd606e079293d16c906a5aa0f7049`

```dockerfile
```

-	Layers:
	-	`sha256:1420fd5a391224485481f3289bea121ceea95b6869b731053173af5eb6a6159e`  
		Last Modified: Sun, 17 Mar 2024 22:28:17 GMT  
		Size: 94.8 KB (94755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e22ca82d24a4a3f67e7928c6c6a9889525b36ed128e501e2fb7a2f5fb5d6f0`  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json
