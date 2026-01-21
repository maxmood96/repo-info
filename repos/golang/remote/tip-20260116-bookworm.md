## `golang:tip-20260116-bookworm`

```console
$ docker pull golang@sha256:25d57eb152e96410d056d7d5b7520ee0f6b800ef1ff38702688341e4b282b89b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20260116-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:59fcbbdd612de73b5049740ddf60a8011d2dd28f2ec41a9847f141b94a6fc3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324404326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378c64be9b9613ad7f92668159d8195e699af7be9241bdef3c2cc77d0210f155`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:50:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:51:44 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:51:44 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:51:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:51:44 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:51:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:51:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:38 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4089a83edea30bffa166b7aa97dbfde35ea28cbdfe9515da31f339b30b04b7`  
		Last Modified: Tue, 20 Jan 2026 22:14:20 GMT  
		Size: 92.4 MB (92433450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b6a5b8343289eb0c3c52bf550e1fe8d1945ce754f136a34955c716ac7e17d7`  
		Last Modified: Tue, 20 Jan 2026 18:52:04 GMT  
		Size: 95.1 MB (95056396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0f20b13c27c0de743b5c848282eb68c9f05ffdf1be0632e7595a075243ec37`  
		Last Modified: Tue, 20 Jan 2026 20:51:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260116-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ae10840d752c71530953ba7c65d562c39d0ae7458db9863b23e83f1063dac57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997bf60c4dba3db5bb98a817f01b9216e4b2db4d40fc11caeaf34e45ef243c7e`

```dockerfile
```

-	Layers:
	-	`sha256:0c1ba535c2f5cda586700ad953527e039541f09ab7726dee8e476aa3c948d190`  
		Last Modified: Tue, 20 Jan 2026 21:25:01 GMT  
		Size: 10.5 MB (10497031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5264f678d25cd31b4681027fff3d8b71b847783466c3c2ddff50daa96c5769e`  
		Last Modified: Tue, 20 Jan 2026 21:25:23 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260116-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:3186ec3c0df4867226c2d8b5487c3e9674ad7fe152fdee02d716f15f8b0964ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283209018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123ac47ca5312204385f18e75b70648d86fad96a795122b934a4d078b114efcd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:50:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:53:20 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:53:20 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:53:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:53:20 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:53:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:53:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:15 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:25 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f9f395cd1e9e02761196527b4253d5246be969781795c278996437891e5cf`  
		Last Modified: Tue, 13 Jan 2026 04:25:12 GMT  
		Size: 59.7 MB (59652006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732bd3cda2c98f5a765e8f2bf0c5251a5c150561ea8abdf70474d6a8f3130e16`  
		Last Modified: Tue, 20 Jan 2026 18:53:59 GMT  
		Size: 66.3 MB (66288734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bbc1ebe88b1983952e0d3b08c79038602b5105dcae7c600fd0a26d7e35cad0`  
		Last Modified: Tue, 20 Jan 2026 18:53:18 GMT  
		Size: 91.1 MB (91127787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db534c9c0dfb124fb593b3c3317ce2f3ecdb498d16933ec451997d78875b5ef`  
		Last Modified: Tue, 20 Jan 2026 18:53:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260116-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:deb22e1b25bf674e8713f18a3795d0942ad3dbac5899c313f3ab79bf8f868ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4d0c9c3a92963de9ba738ce491cc614baf38a3fcb01d4df5e9f910d77846bf`

```dockerfile
```

-	Layers:
	-	`sha256:173db30eadb2abfda57e0674a5e71c73942f86eeb00eeefb297a2154bf964ab6`  
		Last Modified: Tue, 20 Jan 2026 21:25:11 GMT  
		Size: 10.3 MB (10303727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0c0a54ab66c7add5d396340268860511e25c7786f85ada907af60f47fcf625c`  
		Last Modified: Tue, 20 Jan 2026 21:25:18 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260116-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:aa4f6aa6e71dc54a335d336475502ba999c1eac004355d21f388c717f5ed55d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313088954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3dff64954f08800033e1a4c4e9c73cd81829db16d1d11709441ba14a80f6fc5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:50:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:51:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:51:58 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:51:58 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:52:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:52:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:05 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d27b595137e16d3605547ba04381d6712b50c56cb88435ec6b77faaff765c6`  
		Last Modified: Tue, 20 Jan 2026 18:52:26 GMT  
		Size: 86.5 MB (86506489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8704a9b461e9f9c3cf81dacaf53a5375b1bb82e9194e9ce88802dc458b5979`  
		Last Modified: Tue, 20 Jan 2026 18:52:00 GMT  
		Size: 90.1 MB (90131959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ce9f03895b4ad4a65336183d91946fe47fba2e21251cfc2d3d5ffe5f73c573`  
		Last Modified: Tue, 20 Jan 2026 18:52:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260116-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b4a754f59439351fba6efe767de37b45a3192abfb27e3690d32fdbb1b71859ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972ab637e8d8e538fd2d18538bcccff91d3481444f61b2797bf02db8f6cbed0b`

```dockerfile
```

-	Layers:
	-	`sha256:cb426e3bc762036657f79cf1512e1dbee1437c3185dccb338eae40d67c5ccdbc`  
		Last Modified: Tue, 20 Jan 2026 21:25:34 GMT  
		Size: 10.5 MB (10524855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7d4611281dd48b9184f6208919374d6b01af36b995ca9f39b1716cd7013281`  
		Last Modified: Tue, 20 Jan 2026 18:52:23 GMT  
		Size: 28.5 KB (28521 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260116-bookworm` - linux; 386

```console
$ docker pull golang@sha256:ce60f8e49fd2a379d8d8d5149ad222914a081a2c2514c88fd256396ca5b84286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323381213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d121306b77a4e81ce53f8e85c56508ff0f4ba9654bf6d33b297f1977e7796502`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:02:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:50:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:52:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:52:23 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:52:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:52:23 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:52:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:52:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ec54d337d067729b748c8f421e417d2e02e79e9e0caf328deaa1b815a93c883`  
		Last Modified: Tue, 13 Jan 2026 00:42:07 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ef3b5e8322d4c8e5ca6198e931fb91c384bac3ef8aafd81a71617e9534b7ab`  
		Last Modified: Tue, 13 Jan 2026 02:02:14 GMT  
		Size: 24.9 MB (24871330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20be0f262f5ef3547fc45c5726dd33bf707569fc1cceccb9f87c4f4965c4f9ed`  
		Last Modified: Tue, 13 Jan 2026 03:03:36 GMT  
		Size: 66.2 MB (66234261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4055ecf6a2f5917e792e20c0559f985064665252b332871377b67c742f11b8b`  
		Last Modified: Tue, 20 Jan 2026 18:59:16 GMT  
		Size: 89.9 MB (89858830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2898920cb13c505259be6cf40bfc2b763657f2a33b173994b269e661d72ebfad`  
		Last Modified: Tue, 20 Jan 2026 18:52:52 GMT  
		Size: 92.9 MB (92948041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5532946390c3693f22447b5eeae41a1cd37632320a159ea64ece00b9cae6849e`  
		Last Modified: Tue, 20 Jan 2026 18:52:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260116-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e37835d186ce1fb14389dec35d0a7bfc464cece35a786cc9d579fb01b207878d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5358e1c4b476b43e90528f5a3b392b03149288dfe0c0fa45cb2cd2f437e8d84b`

```dockerfile
```

-	Layers:
	-	`sha256:56ab3bd68aa22c5cd200a4a5daa3a2a1b143145044a2c7a13a06c3725766de40`  
		Last Modified: Tue, 20 Jan 2026 21:25:30 GMT  
		Size: 10.5 MB (10476611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:138d5f16d8857035bb9179013e585d4a3c88016e1fd210c7e727de3eccff8141`  
		Last Modified: Tue, 20 Jan 2026 21:27:33 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260116-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:23c90f3c29d1959de278f46d10d5737f99ba0e80e3d119cc3cc85eac0c969f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294527179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04959b54f8f2a36a2e1b65f922a5fbb4cb3a3d3e8d4b6aa3bb2b6d8290e6a402`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 16:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 21:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 22:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 19:11:33 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 19:11:33 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 19:11:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:11:33 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 19:11:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 19:11:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4c94e33bcdbce9a62a95be51a6e5f8ed2efc653e4be8f8f6722aa13d9d65461`  
		Last Modified: Tue, 13 Jan 2026 00:40:28 GMT  
		Size: 48.8 MB (48763393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3ebdc0d40ea56bd8ca0e23bf6a7db8ca22ab77cacf0ba126e24eb42d35c708`  
		Last Modified: Tue, 13 Jan 2026 16:18:00 GMT  
		Size: 23.6 MB (23614652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee435e05dd9c53ddee45b81a8f55939374cd926a0e00239c752bb0832a5f8b`  
		Last Modified: Tue, 13 Jan 2026 21:23:11 GMT  
		Size: 63.3 MB (63309962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659edd573efc55ccb964dda4fd8e0b2b02903c5753a704b10ec114e6a6fa5f32`  
		Last Modified: Tue, 13 Jan 2026 22:44:55 GMT  
		Size: 70.0 MB (70021799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eca1bded26c9137c5cf6ca79118befab372cbfd7138be8cb4b952fb281c4ce`  
		Last Modified: Tue, 20 Jan 2026 21:28:38 GMT  
		Size: 88.8 MB (88817217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9ccf767addf07132593ab1aa848c0578087dca1952ffef63f76dbb5db8ce51`  
		Last Modified: Tue, 20 Jan 2026 21:12:06 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260116-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f809adca3b3fc16b079921a84744ab347583b5d1c24c7b5c4cbe88fd7f5a9a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6140b7facfa35bbc6ac8c4168f6de7f30cf91fabf153bad6e12477bfcc59fe`

```dockerfile
```

-	Layers:
	-	`sha256:2daac72f6b3408e8c46b502b5fa42380aad4d5ab4f3b110d28fcc80aea2d8f8d`  
		Last Modified: Tue, 20 Jan 2026 21:25:39 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260116-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:fd2a185ee62f68772140f0e273f601cc891334875a704e8c801c02005e5617f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (329954768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d29b4933408dd0132f29ba49712039638a88f8ea34da2bf153b70b817a390de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 06:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 08:53:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:54:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:54:57 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:54:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:54:57 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:55:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:55:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2769c4ec4b4d67e8059086401477839f8b9d5a5026dd27df50a3c7ce33b9db`  
		Last Modified: Tue, 13 Jan 2026 03:35:37 GMT  
		Size: 25.7 MB (25670703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5fcb80ea7d84a82ea96c11045a4f40d0943808d5c5334ea90de2f7ed44f4c4`  
		Last Modified: Tue, 13 Jan 2026 06:38:36 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39324acd74abd8d66fc3636cdba0cabcab5132ff369ae8d34e56255bdb262d35`  
		Last Modified: Tue, 13 Jan 2026 08:55:17 GMT  
		Size: 90.4 MB (90428658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daa35feb63e7ef5c9399e73cf4420af92b3279e1deb9e79d9f88735b792386c`  
		Last Modified: Tue, 20 Jan 2026 18:57:07 GMT  
		Size: 91.7 MB (91681857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd646111c5ad28f7fbd4c0cdba986d1d7447f81858765d25e24d7ffd7c69d6b`  
		Last Modified: Tue, 20 Jan 2026 21:58:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260116-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:479f4908df4c2c921894aa5763b7b2858003d043901850b84446cffde56e7faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3904f80b488c05f91a00c21c1d2390714a0c8e13c0c42980ea76f5700ad7129`

```dockerfile
```

-	Layers:
	-	`sha256:68ce32b40d9ee5486e62ee7b8460379ffbf73df9fcfa90ba9e4d51f14df76094`  
		Last Modified: Tue, 20 Jan 2026 21:25:44 GMT  
		Size: 10.5 MB (10469516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f477a86f782069c2b0e0b70f50ba0d702aa55b44a8ad45e1ec5ce922b7bede7`  
		Last Modified: Tue, 20 Jan 2026 21:25:45 GMT  
		Size: 28.4 KB (28431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260116-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:59edd19acae33d0028374307b21fba3abac876ce611b71f3c9425535dba0720b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297923622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9e37cc5d1bf1a935bbfd90300561b4229dc3224025d2f7f7af0884437d9222`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:29:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:53:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:53:28 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:53:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:53:28 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:53:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:53:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8133db08df54d1100dff2f0259f057251959db22c09d939ae558af001aa8088c`  
		Last Modified: Tue, 13 Jan 2026 02:10:04 GMT  
		Size: 24.0 MB (24032491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb4cc23aeea1b258f198103e8c2d450f82da1d5de8a3eb227ed2969f60d97c4`  
		Last Modified: Tue, 13 Jan 2026 03:15:34 GMT  
		Size: 63.5 MB (63501276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ce02e4e54b6659021d8edf907aa6accb7169b9308bca9679853b9c58e085f8`  
		Last Modified: Thu, 15 Jan 2026 19:30:40 GMT  
		Size: 69.0 MB (69018581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee8ceecb5a37e7411922ba0485d5dd3cc40ab1953ffe651cbe56f40f79a249b`  
		Last Modified: Tue, 20 Jan 2026 18:54:10 GMT  
		Size: 94.2 MB (94232686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e380b8f90c511e00b91f803659765e9fe11871e6eaee11447a8841b5d2e15b`  
		Last Modified: Tue, 20 Jan 2026 18:53:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260116-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:cb2b2c35152842c8afd4f6a6ec42ba203808c63a12f80d35193f5d8396bcdb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe9b6de93a6e162477e79f791957cb7085d649fcf32d100eb931b7a45ff76cd`

```dockerfile
```

-	Layers:
	-	`sha256:05fcf984282b55b0f678934be2446ca282e198acb205c6dab63b0855e506615c`  
		Last Modified: Tue, 20 Jan 2026 21:25:57 GMT  
		Size: 10.3 MB (10328789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:062dc170db08f515255ed18ced2c26998a582e54f4707b71e43ad1eaa546cb42`  
		Last Modified: Tue, 20 Jan 2026 21:26:04 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
