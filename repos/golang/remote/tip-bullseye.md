## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:2351784c63afae664d0fe09634a42e90fa54df7fd8c5a57e71afb61304733167
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:855dd37e39044f13aa0b879a6b995908e618bbf4cb342f807edfbaa9d1b3ab94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336924879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f185837d843ffb9bacecc3495f68041b9075813e2916d4910039df2c9efe8777`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f843b455b9b7bececb5cfeb4ba5839d4aa47845ded1258734c375304df3d0`  
		Last Modified: Tue, 08 Apr 2025 02:13:52 GMT  
		Size: 54.8 MB (54755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63840016c6293a52e814fabb67cb9c3330f7fc810bff2253d95a6eb00e17637e`  
		Last Modified: Mon, 28 Apr 2025 18:23:15 GMT  
		Size: 86.0 MB (86001184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65846c33088373b4d6ff39b83056f623dac3e1cb831137df32e4e70bf9d848be`  
		Last Modified: Mon, 28 Apr 2025 18:22:59 GMT  
		Size: 126.7 MB (126656346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799018b74454322a49c0d05687ff96621e82618a47ce2580768ba9e037413f53`  
		Last Modified: Mon, 28 Apr 2025 18:23:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:25ccbd0f876e1d6fd827307ffe345ec18857a2ae58efe204c1130e604bb974b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3341640e7a9d69a403ad4e23db22f72adff9d2ce6a09dca06c6c3f205c3c6d`

```dockerfile
```

-	Layers:
	-	`sha256:79166b0e6ae2b72d28bfcab69cf129d5952f883a14dc68d717dabe0c23805b26`  
		Last Modified: Mon, 28 Apr 2025 18:23:13 GMT  
		Size: 10.3 MB (10266343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a6dc968db1673c4743e02a013acd1deed8071acbb6ff2cb0b8143b432030e05`  
		Last Modified: Mon, 28 Apr 2025 18:23:13 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:2e059a0f0db5791a29e2bd6fdc2e1620571e57188f830b6f296a45cd451ca793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301132123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa574163899a4c549199ef97938af49cd1c95b775430e4bfd482d5823c05186`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b68fed12d763a57f1b020aa1579673112de80a5b780b5ffaa045109c81f23`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 14.9 MB (14878713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909681b45fdfcbd0bfebc28d96cd1bdab32fd85e3af6788b49d9cb80e8ff865a`  
		Last Modified: Tue, 08 Apr 2025 17:30:33 GMT  
		Size: 50.6 MB (50624452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cc995e80cedd9d30db7ba6d1ae52e5693d2c40c74ff9101649c68046e8319c`  
		Last Modified: Tue, 08 Apr 2025 20:43:27 GMT  
		Size: 64.9 MB (64922622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33618dace1ba528dcd7b40e80a4e895530a8d058bda71f5a87abf8312ed70c2`  
		Last Modified: Mon, 28 Apr 2025 18:46:15 GMT  
		Size: 121.7 MB (121674729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6947be0773c0d57071de7c364494caaf518e1856b480ecb7b1cf4b11c8e19c`  
		Last Modified: Mon, 28 Apr 2025 18:49:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:bc48528aa7d288b7f75fcd8b4a5445da86f481f230d50235d209e12d45693acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10099852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60977f997b47d4201ec685cc8b5aa0085146dd5f5f854820ff02b0f1a5df518`

```dockerfile
```

-	Layers:
	-	`sha256:07d96291dfbd6e656424a1444e71a85ab4cd2218411e87d378bf1d80f7fb08f8`  
		Last Modified: Mon, 28 Apr 2025 18:49:48 GMT  
		Size: 10.1 MB (10072683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef555813090430d5dec0980febf928ac920a77a07840c71da93f5d0bcf1729d`  
		Last Modified: Mon, 28 Apr 2025 18:49:48 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1ff07f8b6be5100f8e0284095af9218282cc2e1738de8a6745ed50c89fdf5e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323668070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32b952aac765f11afef8c8073292aca95063933020e2f2c99335ec73d7077cc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b066ec7b453f1f7a4cbf31adea4a73d091a7499693ce31c56205980d8778c9c9`  
		Last Modified: Mon, 14 Apr 2025 21:52:34 GMT  
		Size: 81.4 MB (81414208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280b2cbe9b185a145cd427125ccd35e0250a80679d21036014ab14fdf1e6e707`  
		Last Modified: Mon, 28 Apr 2025 18:48:43 GMT  
		Size: 119.4 MB (119400389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3bb9dfe74b89210637b434b324b6ed4cd13fc161ceb9375c71b6059e4816c9`  
		Last Modified: Mon, 28 Apr 2025 18:51:05 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:1899bccfa0846e5f45608287f699aa6a49366354e79c3dec7830f1fadcfbedc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d42b249e9506cb56807dddba82e1b863fc62b26ab144080e79c991b34f9904`

```dockerfile
```

-	Layers:
	-	`sha256:29e0532199b520b8cdc85de2c43cd18c9c8341c71e48d6c5cf85c30ee1903e35`  
		Last Modified: Mon, 28 Apr 2025 18:51:06 GMT  
		Size: 10.3 MB (10267915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06e64fbef9a1cf9230386b37c721656b2fdf162a0835a2d798a0bfa92f9a807`  
		Last Modified: Mon, 28 Apr 2025 18:51:05 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:0e4e40b840d067aa6bb63fd57e44ca12532b179f743406dc251ea163fa8e0077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339468185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0692ed47301d94887b29200fdb800ef41dd01daef8b9cccb2e9d416e74051d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffef4e17cbc252fc170472ff3910647beec8b91ac9abe188d6595b2087a0dc`  
		Last Modified: Tue, 08 Apr 2025 01:24:12 GMT  
		Size: 16.3 MB (16267037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d7ac3a47d27aefe42d135394e4d8b703fb530ab3bd2ad6ef78b8c9beaf885`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 56.0 MB (56047217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb02d259951ac3bf2bf09e4716534e52dbb23693af65e1f82e2517633488ecf`  
		Last Modified: Mon, 28 Apr 2025 18:23:47 GMT  
		Size: 87.4 MB (87426623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42eb229ffaec8bb2d4ae5f6af15344b1b77eb404d2dcc67eaa5dd80ff2f2957`  
		Last Modified: Mon, 28 Apr 2025 18:23:36 GMT  
		Size: 125.0 MB (125042685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba7bda1cc451e5338e7c58a628af1a13e37601d566cd7fc883b6533efb5624b`  
		Last Modified: Mon, 28 Apr 2025 18:23:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:2c56654eed2e0eca5800fe1bb43a7c84e7a0baddbb6c02b62362e2d43782bc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fda33e0fff273fb2062f74dc549569ea9815569a3195389a9146164ad1f32f0`

```dockerfile
```

-	Layers:
	-	`sha256:20ffdc779261fa7cf31d8a95816d684c471d95d44239e61caa31c7fdf80c7632`  
		Last Modified: Mon, 28 Apr 2025 18:23:45 GMT  
		Size: 10.3 MB (10256134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7763fff3fc7cdaf738ceb329df2f93ba6baa181f5d85ea1ef7a3c415bba9b5`  
		Last Modified: Mon, 28 Apr 2025 18:23:45 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
