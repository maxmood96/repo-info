## `docker:20-dind`

```console
$ docker pull docker@sha256:43741b9aa479ab10fabf947a9b5016b7901142a6b5dd9f1b7716e1a4934fd406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:be20acdedb34b6b09b6f6379c84dffb750b5bb0a88c3b0047a790408e5813b3f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80298066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90109ab0c2dc17a53d4b154aa8295a94338f5a3d044886bd72aa4b5b5fa6cac7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:29:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 05:29:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:29:34 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 05:29:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 05:29:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 05:29:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 05:29:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 05:29:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 05:29:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:29:42 GMT
CMD ["sh"]
# Sat, 12 Dec 2020 18:12:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 12 Dec 2020 18:12:31 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 12 Dec 2020 18:12:31 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Sat, 12 Dec 2020 18:12:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 12 Dec 2020 18:12:32 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Sat, 12 Dec 2020 18:12:33 GMT
VOLUME [/var/lib/docker]
# Sat, 12 Dec 2020 18:12:33 GMT
EXPOSE 2375 2376
# Sat, 12 Dec 2020 18:12:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 12 Dec 2020 18:12:33 GMT
CMD []
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db28d0fdbf69ee580b35224bf77ef5e71f9a061c0aafab87064af9708035d9d`  
		Last Modified: Fri, 11 Dec 2020 05:31:33 GMT  
		Size: 2.0 MB (2039048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292df0bc6bf3350f306af7623bc14f00386239bb27303d3047104b9cfdb55460`  
		Last Modified: Fri, 11 Dec 2020 05:31:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e060f4bd70b333ccaa7ae441b42f1068621b39bbe8eb9c71b5a4e06d10b4ff3`  
		Last Modified: Fri, 11 Dec 2020 05:31:46 GMT  
		Size: 69.5 MB (69457871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e8d568a22304aafab5a456040525abd0b705efad0b6e60e64847ebe1c6e4e6`  
		Last Modified: Fri, 11 Dec 2020 05:31:31 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6ef1a942a0f6b2ab0993eecb7ce30d31f06af50a2ae40893e1a160c9a0892`  
		Last Modified: Fri, 11 Dec 2020 05:31:31 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2312dd95470aa8eaccef80bbca7892390ca777559b50fab574e65147a35107fc`  
		Last Modified: Fri, 11 Dec 2020 05:31:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74c897205648b865ec45efcc0c0be8a3ccf9f3f3f60cc1383d5564c72302e20`  
		Last Modified: Sat, 12 Dec 2020 18:13:33 GMT  
		Size: 6.0 MB (5997645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa8e83a7aeb20771ef165f19449f2733ae1aee4c6efe28b6b2e4109ef65baa8`  
		Last Modified: Sat, 12 Dec 2020 18:13:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b1eb2027ff8834916826431c1bdd26901ee758dfb9877c38275a4e62239295`  
		Last Modified: Sat, 12 Dec 2020 18:13:32 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36cacd847e245cd8b2f813f5cba87f6b5fff177d7845e4cb1b290d27466ebe6`  
		Last Modified: Sat, 12 Dec 2020 18:13:32 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31548ab869bd6fcf73471c44c5332bfef15a90b3bbdabfc8e744f38e3d6d10b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74319177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cf207b112d9f66e003ee80b4be8fc38d493b4a6d3cb2b6097cd3a20273cf98`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 03:42:09 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 03:42:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 03:42:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 03:42:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 03:42:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 03:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:42:32 GMT
CMD ["sh"]
# Sat, 12 Dec 2020 14:05:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 12 Dec 2020 14:05:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 12 Dec 2020 14:05:57 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Sat, 12 Dec 2020 14:06:02 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 12 Dec 2020 14:06:03 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Sat, 12 Dec 2020 14:06:04 GMT
VOLUME [/var/lib/docker]
# Sat, 12 Dec 2020 14:06:05 GMT
EXPOSE 2375 2376
# Sat, 12 Dec 2020 14:06:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 12 Dec 2020 14:06:07 GMT
CMD []
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b718f631fe67ed5c2ddee0ac1f74cb77a1211022efb33aa66f6f5d6d2f05f`  
		Last Modified: Fri, 11 Dec 2020 03:45:09 GMT  
		Size: 63.6 MB (63558264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938160415222146a455ed7ddae6e01d0c41f91a764f77ac05ed9794d08adf6a`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb6da89ff942a1c917a6a29653eb45dfc3826f334b16e17bc82207ce1193cc4`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70c0c122f402fb4ee26f6661b037f3e6ee30e639f710e4f318dbf908e60a65`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8afd8df3b7cdec4857f13fd9220eedddfec97a9b472d534b64c3061aa30cf6e`  
		Last Modified: Sat, 12 Dec 2020 14:06:56 GMT  
		Size: 6.0 MB (5986441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eff5b3d64e850cc6162e025f1861c218b1a6db4195963699adf17792510be4b`  
		Last Modified: Sat, 12 Dec 2020 14:06:54 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1864e7f84e2dee54ed6b17a27027327bef427f36ab47cc9a02a3fce44e887103`  
		Last Modified: Sat, 12 Dec 2020 14:06:53 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b60a743d62dd15c7c619c9a7c6940cd70e8efc3edf8fda03009c9be8301e1`  
		Last Modified: Sat, 12 Dec 2020 14:06:54 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
