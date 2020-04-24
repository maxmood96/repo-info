## `caddy:builder`

```console
$ docker pull caddy@sha256:93ff7fdd291e91305f3269e2855fc1ae094d08c3f44d7945033e999f6a63ba36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:486d86fe70265203228afb9b9e6e7934019090c6686da9a9fb98579931a05778
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322863984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fd06ca5bdeb1a36375ba63a93a06401045ebb7a6154830e973a6de5949242b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:02:02 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 23 Mar 2020 23:02:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 08 Apr 2020 23:06:10 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 08 Apr 2020 23:11:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 08 Apr 2020 23:11:13 GMT
ENV GOPATH=/go
# Wed, 08 Apr 2020 23:11:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2020 23:11:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 08 Apr 2020 23:11:16 GMT
WORKDIR /go
# Mon, 13 Apr 2020 23:43:21 GMT
WORKDIR /src
# Mon, 13 Apr 2020 23:43:23 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 13 Apr 2020 23:43:24 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0-rc.3
# Mon, 13 Apr 2020 23:43:27 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Mon, 13 Apr 2020 23:43:27 GMT
WORKDIR /src/caddy/cmd/caddy
# Mon, 13 Apr 2020 23:43:57 GMT
RUN go get -d ./...
# Mon, 13 Apr 2020 23:43:59 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Mon, 13 Apr 2020 23:43:59 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c732a2540651eb09faab95b03b3b5928ab23e096fae0006bdc2abf9e0cb5bfb4`  
		Last Modified: Mon, 23 Mar 2020 23:13:03 GMT  
		Size: 301.3 KB (301283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2225181d6bcfb7877529a7257ff207cb14e52831420f770cbc2187031b6228`  
		Last Modified: Mon, 23 Mar 2020 23:13:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdfa13e5b48c976ba308826b27a4978c2ffe6833efcfcfc0bd40dbf25e88455`  
		Last Modified: Wed, 08 Apr 2020 23:26:23 GMT  
		Size: 132.0 MB (132012220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c48a539365d2d572e18de4a42ab11b02d9870a17bf1f65160d7fcbbd0423263`  
		Last Modified: Wed, 08 Apr 2020 23:25:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947fdad36c6d1e2fd7b618aa1a49dfabaa1ff9d6fb85a195e2437c2b9ac78142`  
		Last Modified: Mon, 13 Apr 2020 23:44:26 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199e6b2236a218d72efd03fc1fa0971c00c87439722e1a40269b7edfd910b79`  
		Last Modified: Mon, 13 Apr 2020 23:44:28 GMT  
		Size: 8.2 MB (8155831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732862f7439776bbe7cc313ed1e10454506f168429234c0daea17d6c48a9692`  
		Last Modified: Mon, 13 Apr 2020 23:44:26 GMT  
		Size: 2.7 MB (2744273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54fb1573600e831b250c83cb9dc699bab8aa12040568d9ee542fb8d09c1d99`  
		Last Modified: Mon, 13 Apr 2020 23:45:02 GMT  
		Size: 176.8 MB (176846093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e336ec02e20348f57d1ef8151ecfcd216777f5489f01b29164883ec496bcbb`  
		Last Modified: Mon, 13 Apr 2020 23:44:25 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6f8a2da1c847ae8cd10d1f3e37ad75cc0ba17c5e9b4f7e68fdd3b7cffb5482`  
		Last Modified: Mon, 13 Apr 2020 23:44:25 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:c9e71494cec26fe243c54231ae6fe4612a24fba7642b2782a2003bd4ac925f77
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318301249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b7f3bccf28346106c5d13d871e3b568057fec490d1f94bb04447e57ff90fd2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:43:41 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 23 Apr 2020 17:43:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:43:45 GMT
ENV GOLANG_VERSION=1.14.2
# Thu, 23 Apr 2020 17:49:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 23 Apr 2020 17:49:50 GMT
ENV GOPATH=/go
# Thu, 23 Apr 2020 17:49:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 17:49:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 23 Apr 2020 17:49:53 GMT
WORKDIR /go
# Fri, 24 Apr 2020 00:01:08 GMT
WORKDIR /src
# Fri, 24 Apr 2020 00:01:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 24 Apr 2020 00:01:22 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0-rc.3
# Fri, 24 Apr 2020 00:01:47 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 24 Apr 2020 00:01:52 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 24 Apr 2020 00:04:31 GMT
RUN go get -d ./...
# Fri, 24 Apr 2020 00:04:38 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Fri, 24 Apr 2020 00:04:46 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ace047eafbdd1d41e753db1fd1004be452f749a7de56a3d24b2614a64577f5`  
		Last Modified: Thu, 23 Apr 2020 18:03:18 GMT  
		Size: 301.6 KB (301629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d0031acb1953f56f2c2592c1c5882b29aa828d45deccabbb9a1b5483090a43`  
		Last Modified: Thu, 23 Apr 2020 18:03:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851f1e9e77f7c701487b8ba5a7a0c915267b412d298572641c41785cacdb0a87`  
		Last Modified: Thu, 23 Apr 2020 18:04:01 GMT  
		Size: 128.1 MB (128149566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8512d94a71aa9475406b77a5df2ea5a15483204ab412358643fbe90c4af6c63`  
		Last Modified: Thu, 23 Apr 2020 18:03:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d515fa8cb76d9c64fedf8066a5d83b006a3f31d3f77bb6fda67c2e36668c18ab`  
		Last Modified: Fri, 24 Apr 2020 00:05:13 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14562a711f9706a0fb683480cf3849913e6b3f11d3599c62e4d1f9e831a46bf5`  
		Last Modified: Fri, 24 Apr 2020 00:05:12 GMT  
		Size: 7.8 MB (7794673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b172f9b87cc50b54dd1b3ec4a0a0d2e28b44b924e8f0602b2ba7a1a93987237d`  
		Last Modified: Fri, 24 Apr 2020 00:05:10 GMT  
		Size: 2.6 MB (2583752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfbdcf6d6318b0e66c309c8d344563f2c4c5fada8a8764f7b513dbecd956170`  
		Last Modified: Fri, 24 Apr 2020 00:06:03 GMT  
		Size: 176.9 MB (176850568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb35003bc5bd2fabea9a8e09f2761c662d1ce95e5d3e829a07ea2b619b5e35e6`  
		Last Modified: Fri, 24 Apr 2020 00:05:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba293916f1b61d0eee5c397f11e2e206ffaa0c54d17f2bfb328da7e6f09743`  
		Last Modified: Fri, 24 Apr 2020 00:05:10 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:e09a9d633f0ac3f7edb608fdca7cb3afdc3d9b594bf776acef1e510665dc9fc7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (316957986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3123713e503402ee579572801ba8280818b09be1916041f92c9ae5169598cddf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:27:40 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 02:27:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:27:43 GMT
ENV GOLANG_VERSION=1.14.2
# Fri, 24 Apr 2020 02:51:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 24 Apr 2020 02:51:38 GMT
ENV GOPATH=/go
# Fri, 24 Apr 2020 02:51:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 02:51:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 24 Apr 2020 02:51:44 GMT
WORKDIR /go
# Fri, 24 Apr 2020 13:44:27 GMT
WORKDIR /src
# Fri, 24 Apr 2020 13:44:30 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 24 Apr 2020 13:44:31 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0-rc.3
# Fri, 24 Apr 2020 13:44:34 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 24 Apr 2020 13:44:35 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 24 Apr 2020 13:45:27 GMT
RUN go get -d ./...
# Fri, 24 Apr 2020 13:45:34 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Fri, 24 Apr 2020 13:45:35 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a35d9f7887ef683587262c6f5ed88364f59775ff882c71bde03cc59f382ffd`  
		Last Modified: Fri, 24 Apr 2020 03:39:46 GMT  
		Size: 300.6 KB (300593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce21b09ea3d1107df35d9f41a664183faabfc461b8f093ab8e9a34d91e8e71b`  
		Last Modified: Fri, 24 Apr 2020 03:39:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf1fed1fc5ff3647312ce126e166e23fb9f96e28f38884ea9873d7f8a316b53`  
		Last Modified: Fri, 24 Apr 2020 03:40:28 GMT  
		Size: 127.8 MB (127774622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8d529407ee4680924c260b8b273f91677815c3930ac19883af92083ca1a780`  
		Last Modified: Fri, 24 Apr 2020 03:39:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463e7353f053210fe6b6ec00c9acbf9e79b9ea985e4ee0d5b95fcab260b69991`  
		Last Modified: Fri, 24 Apr 2020 13:45:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a2c2b3678ca1e9fe82184c0a66d43e7a788dd3b58ca82c700b7d7b205c223`  
		Last Modified: Fri, 24 Apr 2020 13:45:54 GMT  
		Size: 7.0 MB (7026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7325bd77af0abbbd967908e4cea3a497332276ec87420d8f4ebfadfdfa78467`  
		Last Modified: Fri, 24 Apr 2020 13:45:53 GMT  
		Size: 2.6 MB (2583740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f03c9797285c49f60b349379aecfec74a4d5581b170cbd1165a819506fdba5`  
		Last Modified: Fri, 24 Apr 2020 13:46:36 GMT  
		Size: 176.8 MB (176849066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903911b51a8dd7b3049a4cdb36cd8f86bfee4713da4a29af05b69ec942b9e836`  
		Last Modified: Fri, 24 Apr 2020 13:45:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bafd16def92e4dadcabefaa9a11a02ae6b1ba0061faa32f119203993b0dbc`  
		Last Modified: Fri, 24 Apr 2020 13:45:53 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e75235cf1774ab1a9cf57679d190475b11a5e183ded36f466636b129f6eff4ce
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 MB (317231139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6268a533de6eb3c1282aa6480e5b8b5456bbdbf96c85689fac59b9e4b8ee9e1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 09:30:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 09:30:23 GMT
ENV GOLANG_VERSION=1.14.2
# Fri, 24 Apr 2020 09:32:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 24 Apr 2020 09:33:01 GMT
ENV GOPATH=/go
# Fri, 24 Apr 2020 09:33:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 09:33:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 24 Apr 2020 09:33:05 GMT
WORKDIR /go
# Fri, 24 Apr 2020 16:37:05 GMT
WORKDIR /src
# Fri, 24 Apr 2020 16:37:08 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 24 Apr 2020 16:37:09 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0-rc.3
# Fri, 24 Apr 2020 16:37:11 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 24 Apr 2020 16:37:12 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 24 Apr 2020 16:37:42 GMT
RUN go get -d ./...
# Fri, 24 Apr 2020 16:37:49 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Fri, 24 Apr 2020 16:37:49 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fc45ca0357821724e2824e141e2062d236dedad3d8654e0a390419ec9fe393`  
		Last Modified: Fri, 24 Apr 2020 09:38:53 GMT  
		Size: 301.8 KB (301770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332e392c90a454bd9f70a303cda942eb0e131e321e82cb70b9346ece4a52a64`  
		Last Modified: Fri, 24 Apr 2020 09:38:53 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f4526528e3f6ae0b8c71779d660d4b102620e94433d0c4f6947916633995e6`  
		Last Modified: Fri, 24 Apr 2020 09:39:19 GMT  
		Size: 126.4 MB (126405852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ee41552244ce7a16b4e463105b5589cc09a8db04bfbe50ff7225cde4cdd451`  
		Last Modified: Fri, 24 Apr 2020 09:38:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563a0747953abe39285173699e5f790697a6be2542ba5e0f5b16192d0912e2f0`  
		Last Modified: Fri, 24 Apr 2020 16:38:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69aaff34b0ef81b132484a7de376ce72b73f8a83989082d5fc96a2aa0fe3d9e1`  
		Last Modified: Fri, 24 Apr 2020 16:38:13 GMT  
		Size: 8.4 MB (8365426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aeff2961fec9e30c07b1c06df252eda5513c7c330c29fa776b6074901ead289`  
		Last Modified: Fri, 24 Apr 2020 16:38:12 GMT  
		Size: 2.6 MB (2583741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea359823b09de9375640353454a09a847796868aefe01f79e1c115aa0ebed93f`  
		Last Modified: Fri, 24 Apr 2020 16:38:51 GMT  
		Size: 176.8 MB (176848799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369c2b2586913fada7f9390b35d9ac64384dac9b14fdcdfae0e36256577ffa08`  
		Last Modified: Fri, 24 Apr 2020 16:38:12 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339bdcaeb39da9dcd61b5526b5879351d4c6970db8f22150bfa83ceb6b74b1a9`  
		Last Modified: Fri, 24 Apr 2020 16:38:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
