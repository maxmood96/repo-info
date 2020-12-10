## `docker:20-dind`

```console
$ docker pull docker@sha256:966fa8ffc906db545cc63c8522d690fc3d2f532ed41e38cf77f6899577202b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:e3fce5a4c98c04f4a87ff99f8685a7786c7e6f56dbf8fe84361d18243c3e3dc1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80259056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac4603edb9dd6d085df3c3316b52823a8bd3a8ecee36596b57cd555b1daee12`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 16:34:06 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 16:34:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 16:34:12 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 16:34:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 16:34:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 16:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:14 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 16:34:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 10 Dec 2020 16:34:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 10 Dec 2020 16:34:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 10 Dec 2020 16:34:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 10 Dec 2020 16:34:23 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 10 Dec 2020 16:34:23 GMT
VOLUME [/var/lib/docker]
# Thu, 10 Dec 2020 16:34:23 GMT
EXPOSE 2375 2376
# Thu, 10 Dec 2020 16:34:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 10 Dec 2020 16:34:24 GMT
CMD []
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad174ccba36b8f14fcad7acd2d4d4a6a70c78b7fa49a623f8b8557dc616c0a`  
		Last Modified: Thu, 10 Dec 2020 16:35:25 GMT  
		Size: 69.5 MB (69457839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b7b4f00962396937d4369b06af34f2073df4a8a064f8935ca92d0074284ee`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b74a9be2796df0a72ded657580f6ae7e7631a9bc137290cbf5b8313913404b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2fb13aee8fdf8087cc7a884f3e48b6b638fcad658ff007355fd98299d9da58`  
		Last Modified: Thu, 10 Dec 2020 16:35:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7f82b21c3f8cd9e39611558afa5804c6fe4af0b75efa09a798f8f9a1054b2`  
		Last Modified: Thu, 10 Dec 2020 16:35:34 GMT  
		Size: 6.0 MB (5958739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562727d5d45b1d0ad2d592d2a2a15f3b198f41de422c656c7979c8318f0ea5bb`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba03660489307ad179906e45183b116c9427f8ddead0f662b9e7b5db78c3d67`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad80ee751f5b6255560a041c939c5e9e0e1a8648c1883d2664e44a5ee5a82f`  
		Last Modified: Thu, 10 Dec 2020 16:35:33 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:276e1b2f773c7827c7b736fd0eaadbcec4a79ef6e11541c4f91e05ae51412890
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74279441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aac698816bffef06f95633af86828db2aaf96b8de487ee707aaa8859c072239`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:50:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 02:50:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Dec 2020 15:51:48 GMT
ENV DOCKER_VERSION=20.10.0
# Thu, 10 Dec 2020 15:52:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 10 Dec 2020 15:52:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 10 Dec 2020 15:52:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 10 Dec 2020 15:52:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Dec 2020 15:52:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 10 Dec 2020 15:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Dec 2020 15:52:22 GMT
CMD ["sh"]
# Thu, 10 Dec 2020 15:52:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 10 Dec 2020 15:52:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 10 Dec 2020 15:52:45 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 10 Dec 2020 15:52:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 10 Dec 2020 15:52:49 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 10 Dec 2020 15:52:52 GMT
VOLUME [/var/lib/docker]
# Thu, 10 Dec 2020 15:52:53 GMT
EXPOSE 2375 2376
# Thu, 10 Dec 2020 15:52:54 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 10 Dec 2020 15:52:56 GMT
CMD []
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85db56a0506354d758e7aa37b41ef4fff997520e3bad443abf5a31e7e71d779f`  
		Last Modified: Thu, 22 Oct 2020 02:51:51 GMT  
		Size: 2.1 MB (2061246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb67d6aeaaac2f2df73d644bd7912b4e92743c2520751feb04af77d3c76ff5b`  
		Last Modified: Thu, 22 Oct 2020 02:51:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078a48a8a50a1592e5db160ac2c936ff7f08a32ec0cb75ac7f4dffe93632e8ac`  
		Last Modified: Thu, 10 Dec 2020 15:54:01 GMT  
		Size: 63.6 MB (63558290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158a5e5655212749b6eac337022906cbd53a1ed0f858b6de64e70b72814f03c1`  
		Last Modified: Thu, 10 Dec 2020 15:53:39 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580500bbad4eca66986d3601de67b057202691ca6663fe3edf6430a159785836`  
		Last Modified: Thu, 10 Dec 2020 15:53:39 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2dce50f859a7e46b61053c9dd96461e7b0e99ad41877436327e44c77f09d19`  
		Last Modified: Thu, 10 Dec 2020 15:53:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ad112735e0e43f066bb1b5928137e2929a59dc8930859aa13f9de58eecac44`  
		Last Modified: Thu, 10 Dec 2020 15:54:21 GMT  
		Size: 5.9 MB (5946730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73731f39706d7bd5311bda568f910a605e4acf251f39ad9cb88368fb26ff5d4a`  
		Last Modified: Thu, 10 Dec 2020 15:54:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03207733c80702fff03292ace4af276a4553208ccbdde959c1c43ed1d58c660f`  
		Last Modified: Thu, 10 Dec 2020 15:54:20 GMT  
		Size: 934.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e33b2ca44fc024c9d8798a62350b37d8d0ebf76a380d15111bd85530aba6477`  
		Last Modified: Thu, 10 Dec 2020 15:54:19 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
