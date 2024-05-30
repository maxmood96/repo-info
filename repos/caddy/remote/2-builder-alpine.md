## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:bdfd9eda328f615f3948329761abc99013772fafb97c6c41bb882815a11d322f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:1d97a1bfc689534068bc99b432822dc9842c649e729cc0c154f8c154d63f45b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eb6b1b4823de1adba6bebfdf129c46e2b64995736eb6673f1ab8feb5553ee9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e402b0dc7c1ee13bd10aeed32ca6f6730dfbbd53b36df1c2c43ba6c1ac0ca1a8`  
		Last Modified: Wed, 29 May 2024 23:01:15 GMT  
		Size: 5.9 MB (5914555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4feb0354e90f2c326e6b7d6e8aa8f0c14cb5cafeedd520bbe661cbcdc54876`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 1.5 MB (1500672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6a145aba22dc1cdd83e6e4bc89d3dcd83fed07b9df5447bb29107c926a4222`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a53a011c1a5f9f4482d50088c1170f9d734d111fd6e53b13901390301dbc987a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502eef3ba542c157731565e6b10b6f605c5bbaa4cb2f1a8aa0fcea2fe89d7105`

```dockerfile
```

-	Layers:
	-	`sha256:b40a1d307eafd54bf402058964d29328638bc46540b1ff0e89cfafd693be59c2`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008d2100174b1ae9d0f0f9e9dac7a9d327aa68c96b29fb0f6f7eb63a109c8d9e`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:76b024f4bfc423eed7169d9548312432f113ec180d6fe4abf9dea3056f08e013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f41be2f19d58f1bc9f7f405236e380a2cb5591a9f3861c7f8f42818200283`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b97bf58febbeb200aa9d2afef8fe6cd7c0ec7c32c2924df16f50e5b908515`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 5.9 MB (5863420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60932c3d4c230ff0adc1536a623aef6a7587fbec36b8add10672330287c9ad0`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e115e84021acc84d0da9a8c93309a09a344ee4fb560abec304c2c599386f62`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3461e07084978dfa05c463d289dc6dbd055b41fd9e6b22f8f58c976d1d3cb9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a214bf5aa952a1965e3eb6e089d2e3d6c4e0cf8cf288c820163d16eb47481c41`

```dockerfile
```

-	Layers:
	-	`sha256:8c82281543d077f647436232fe98bb809e9db5bbe6cda5cae4f0916f0b000d43`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:09a6c1b0e1bd5044d5c064715c0aa03b90e6940ba650cf16faef929b3f79fa04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74794769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a0acea946d5a81787cb9fe18c7071c5aa68a591344d13571c0ce51a5e470d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1e32b4becad7a3ff9750dab0a6195a4136fe3417839cd5d6ced26f77c37d79`  
		Last Modified: Wed, 15 May 2024 08:39:33 GMT  
		Size: 293.0 KB (292954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab304151744566becd5140e866f02946274de2d4d2a228bdba72a0e4dddfa248`  
		Last Modified: Wed, 15 May 2024 08:40:52 GMT  
		Size: 65.8 MB (65766163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ceb4452378bf5d66c4470fe48fe8427a79ec5fdc8ddb8ea1c7fc02a13ce65b`  
		Last Modified: Wed, 15 May 2024 08:43:33 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270f12d361d5c63e9937439d8ff8f1080a9e9af98e31682da7f8d67a613c759`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 4.5 MB (4515403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058f91ac0045b9c67e0b445141195571ad95b6f59a25eb681889ad831b1498dd`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 1.3 MB (1318268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4d6b7782ec5dfb52798f8e6b9b9ab819fa68f6eb20afac4a297ba01be2efae`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7642ba203742b9113008f284cfdf3548460cbae2ee69ecb2454eb8c735b96da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 KB (291146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94a8f15a57f45b959c2c2fc76cdd718d5ad776676b941690a80ec419f5487c6`

```dockerfile
```

-	Layers:
	-	`sha256:d711709c34958acee3c07ef7e1919d12e4928a2ca18487dd1819cbe2b91d6ae5`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 270.6 KB (270635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41bcb88e50c5a338a29305fce33e34c339529ad379da7ba7d1cd2088bf08e935`  
		Last Modified: Wed, 15 May 2024 09:20:10 GMT  
		Size: 20.5 KB (20511 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:022c416ba80bd913b0d16582f1065f5c4b8ad34f219855b8a021c94d106524c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74098271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d00e35d265158288ca2a81ad2fdfbedc5b7035f13ab9cd1b998d4991d8fa37`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84613e011ca8867fd82ad1a4602a9c5ca1629a8c52b91548ba0a8ce39bc63bd6`  
		Last Modified: Wed, 15 May 2024 10:25:13 GMT  
		Size: 295.8 KB (295843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a7eb7dd16a3cb705d643f2c1b3ccb0cce9120eef39b1b1844864195af6c32`  
		Last Modified: Wed, 15 May 2024 10:28:17 GMT  
		Size: 64.1 MB (64106287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788e89ea89d463b8bcafc4d5b552bddaa08b72930505c3e5b6917da512bca47c`  
		Last Modified: Wed, 15 May 2024 10:29:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5119b2251effb8f032617ef72426ede6300a48b24df3322f8180c5112fcb1488`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 5.1 MB (5063898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab86c9ac1c04673c91199de9df55b222aeb76d630df93b84c38cabab987ca9b`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 1.3 MB (1298290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e12372ead2b5522c0b9d32638dcec3d9780a4b4495fe0327787759f670419`  
		Last Modified: Wed, 15 May 2024 17:32:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e620ba0bef62789334c010b7cacf7a13de0927228fc5d74634b118f93d8a5ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 KB (288452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988be65311a6efef34a6bdac2f8dcba490cc5ae7a90c13a7b4b72cd68956fd79`

```dockerfile
```

-	Layers:
	-	`sha256:b860d1f348c1e8c34388faf32ca1f31601f367503a56b8482f22e27d112f725c`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 268.0 KB (268038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0144585ac3a8859d627186fb46c2dc5e2e025006a8801d6718aca937f207427`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 20.4 KB (20414 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ed5114faaef7109c9b6d09463fe6cd92b3012e1b89d7d4881ba567e2215f37c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74339423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa437d1d5649dee8d678ada0475d1bf336545ad8ffa4a692c19bba4fe496c25f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b2216e014970a83beea11c197a24ccf7f0027acc0d35a08b3a3b2c976b5eff`  
		Last Modified: Wed, 15 May 2024 04:47:32 GMT  
		Size: 296.3 KB (296270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b672324861585f05676c004287c9eeb3ec624b063c08e6689139af3a2f1ed3df`  
		Last Modified: Wed, 15 May 2024 05:01:36 GMT  
		Size: 64.1 MB (64129414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4969b1c1838dc52cc8a18a048524a037b980febaecd9563210c4df1a96604b42`  
		Last Modified: Wed, 15 May 2024 05:23:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abcaf0a32c421ab0105f8a6eb25fa2862e92a57fe5c68c0de96702a1496789d`  
		Last Modified: Wed, 15 May 2024 06:09:04 GMT  
		Size: 5.3 MB (5270859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14972492f5cb274941b32172d5bccee08aba0eb45858ff97fe6fb9f45719fed`  
		Last Modified: Wed, 15 May 2024 06:09:04 GMT  
		Size: 1.3 MB (1293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad16cdba266ead2ca15865cafeddfa415df7136a8ea60d18e820ce12c1407b61`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2b40a03abefdfce61a9c05a652fbccf303ce8b02a57d74d4a4e0b3faebc448e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7793b7cdf8a3c9fe0b5515824960473b044a9be5b121a8763e7f63d45e27617e`

```dockerfile
```

-	Layers:
	-	`sha256:a992b851d066d8fb1da7d613d1d07540e1edd799d4b99a7da6d8c73629f8982c`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 266.2 KB (266157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b35b875bfd977ef42a74ac4b84ec1b6d05e4daea22d2a52db56fab59e5a6663`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 20.5 KB (20460 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:e53c2ec5bc7bb3e46c3b08cbe2793d45479d1264c40b5503bef29eac2c91bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3723281c06eda99cbaeea6f288865cad6be253c3b7ed970ae0073b1cff680a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbea9d4fd6b7817ea21385211ac68cd734b6e36168539fdfc45a17147cdfbeb5`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 1.5 MB (1451783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd654ccf1647a25716cd5ade72e99d159e39c702b954bd5e1e628ad8095cbc7`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:208946b4132505ebe3d024e76404801b3efceaa335e267fc1147680e4d0a72dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba39e663c5c23602c18674f4c908a2b81d5f5fce9def8350942c92d2c701d6`

```dockerfile
```

-	Layers:
	-	`sha256:726f8c49f1c023380c093fbb8f09dfe9021e323fbdbef3ad8057b76e18e391dd`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97dd399ce6968f36de5122b2b40bebfdca47410eb2e2264e7dd75c76b02ca0e`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json
