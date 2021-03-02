## `docker:20-dind`

```console
$ docker pull docker@sha256:2621d6bbfd3a63d6ebdde174782c353620c6cd8b960438c0c18c1c1d292b2de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:203e6241167f0f429b6059700dad917712d882dc7eed804c799b3d66a5570614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80944296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3052dea93a5a9ecba2e2c33d4ee11f0d5813f767dff6763e06ddfd4d2ad836c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:43:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Wed, 17 Feb 2021 21:43:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 Feb 2021 21:43:05 GMT
ENV DOCKER_VERSION=20.10.3
# Wed, 17 Feb 2021 21:43:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.3.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 17 Feb 2021 21:43:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 17 Feb 2021 21:43:12 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:43:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Feb 2021 21:43:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 17 Feb 2021 21:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:43:14 GMT
CMD ["sh"]
# Wed, 17 Feb 2021 21:43:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 17 Feb 2021 21:43:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 17 Feb 2021 21:43:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Wed, 17 Feb 2021 21:43:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 17 Feb 2021 21:43:23 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:43:23 GMT
VOLUME [/var/lib/docker]
# Wed, 17 Feb 2021 21:43:24 GMT
EXPOSE 2375 2376
# Wed, 17 Feb 2021 21:43:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 17 Feb 2021 21:43:24 GMT
CMD []
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94caa5d1da7043140e78e14956c22154f75708f44c1c1367ac20cc5a8be71e8b`  
		Last Modified: Wed, 17 Feb 2021 21:44:58 GMT  
		Size: 2.1 MB (2051413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10a29983da5ea49c724d6c132f4d3dc6c130fe7148e4dd9fc258c34fa210f0a`  
		Last Modified: Wed, 17 Feb 2021 21:44:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b071e807615fb6b532dfdd17f2a8e762342b7c7fab8bbe4a4a5955b6d96cf446`  
		Last Modified: Wed, 17 Feb 2021 21:45:11 GMT  
		Size: 69.5 MB (69464299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e312d1fdaab9b3c93108fea6ae5669f6d02901ecb9058c69c26593aee6f5552c`  
		Last Modified: Wed, 17 Feb 2021 21:44:57 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22fb1b38bf3caf7fae8aad8e222981e7966663ecee232b6334e76249468e122`  
		Last Modified: Wed, 17 Feb 2021 21:44:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c60ac175054247b429aa833807d437b110d11a1bdde9d6ec24a8d164625291`  
		Last Modified: Wed, 17 Feb 2021 21:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91afbfdd7b778c4bcfb1fc9f2d924472ec7b3b5e54791e67aa381c4886d16641`  
		Last Modified: Wed, 17 Feb 2021 21:45:20 GMT  
		Size: 6.6 MB (6610375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babfe5fbbe656c5603a4e594447041fb6b8765352a706152ff18a50e3a13bf99`  
		Last Modified: Wed, 17 Feb 2021 21:45:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c24736699a6eae917e05f208d8a6450d5c98b08a66fc175c6579de3a9fbf68`  
		Last Modified: Wed, 17 Feb 2021 21:45:18 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c37595645aaccbdfdc23d0f2ecd36c298273ee86bc09dbbf3c622172496630`  
		Last Modified: Wed, 17 Feb 2021 21:45:18 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3e51712955448c3ff70f2bfef5111489c9daf2d663d218a06463301dd6f87d1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75075113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba573097f6e9b53b36d3881dd1385bc42e0811f17f7c19b114b6ba4a8b99d5b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 20:58:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Wed, 17 Feb 2021 20:58:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 01 Mar 2021 23:39:55 GMT
ENV DOCKER_VERSION=20.10.4
# Mon, 01 Mar 2021 23:40:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.4.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 01 Mar 2021 23:40:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 01 Mar 2021 23:40:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 01 Mar 2021 23:40:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Mar 2021 23:40:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 01 Mar 2021 23:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Mar 2021 23:40:08 GMT
CMD ["sh"]
# Mon, 01 Mar 2021 23:40:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 01 Mar 2021 23:40:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 01 Mar 2021 23:40:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Mon, 01 Mar 2021 23:40:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 01 Mar 2021 23:40:25 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Mon, 01 Mar 2021 23:40:25 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Mar 2021 23:40:26 GMT
EXPOSE 2375 2376
# Mon, 01 Mar 2021 23:40:27 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Mar 2021 23:40:27 GMT
CMD []
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73c8b9b1c8dd10c5e507fe99a317a8c9e76be18ce77b09351cae695d685c7b5`  
		Last Modified: Wed, 17 Feb 2021 21:00:33 GMT  
		Size: 2.1 MB (2067994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10cdebbd0f7f08e6238d70b00cc96942f37974ae2ad8d72478ccef46d019ff2`  
		Last Modified: Wed, 17 Feb 2021 21:00:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bd2b87d1e06a1b11c35a89ca3ff9f38705eab3e83d44917cf290590d89943f`  
		Last Modified: Mon, 01 Mar 2021 23:41:38 GMT  
		Size: 63.8 MB (63776320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7413e673abc99218c2a0fc2e4c62a3bac63ea5d6ca2234b19fc3e4d07a66a918`  
		Last Modified: Mon, 01 Mar 2021 23:41:18 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce18afea95decf6d9699efa49d5f84a0c1146f90a9e82642a30a0e7dd001571`  
		Last Modified: Mon, 01 Mar 2021 23:41:18 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59613af2e94e7657f258e22658ee076d54f3cee7fae4e4572dee82124e637da`  
		Last Modified: Mon, 01 Mar 2021 23:41:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b486067296eb4634e5e2b2f90ec633b804f30a3fe78eeca337b17f690487aab7`  
		Last Modified: Mon, 01 Mar 2021 23:41:48 GMT  
		Size: 6.5 MB (6512612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a508473810acd03bce0ebbe47eb4c993125f449aa5a1daf6b0626d706d75398e`  
		Last Modified: Mon, 01 Mar 2021 23:41:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeee9e9fc380a12deeae981cb5cf7d2073a74c8da65f7ff2228185adaf0a055`  
		Last Modified: Mon, 01 Mar 2021 23:41:46 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569567c6bd299302039d77d0f257c0cd056f03c51ccaec4e151163c176ab26ee`  
		Last Modified: Mon, 01 Mar 2021 23:41:46 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
