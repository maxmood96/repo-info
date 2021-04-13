## `docker:20-dind`

```console
$ docker pull docker@sha256:2636ec38c4567671b24f35683a66d1204bbeed208873a2a11c64dd592742b97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:95a8e1aaf652c8b2c129495964eee8a3b95ed681f3cd85505b4c82f3508b0561
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81649492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b83b687d756362c574f75cfba587172af6cbcdd4d009ecb6d891da9522298c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 12 Apr 2021 18:20:49 GMT
ENV DOCKER_VERSION=20.10.6
# Mon, 12 Apr 2021 18:20:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.6.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 12 Apr 2021 18:20:55 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 12 Apr 2021 18:20:55 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 12 Apr 2021 18:20:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 12 Apr 2021 18:20:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 12 Apr 2021 18:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Apr 2021 18:20:57 GMT
CMD ["sh"]
# Mon, 12 Apr 2021 18:21:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 12 Apr 2021 18:21:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 12 Apr 2021 18:21:03 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Mon, 12 Apr 2021 18:21:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 12 Apr 2021 18:21:05 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Mon, 12 Apr 2021 18:21:05 GMT
VOLUME [/var/lib/docker]
# Mon, 12 Apr 2021 18:21:05 GMT
EXPOSE 2375 2376
# Mon, 12 Apr 2021 18:21:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 12 Apr 2021 18:21:05 GMT
CMD []
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bf0480751fb742e99eb729fbbf3b816a2fdcdd6460ac0802127e69f5cf7243`  
		Last Modified: Mon, 12 Apr 2021 18:22:15 GMT  
		Size: 70.2 MB (70170175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea609d09eab314b7c057381499784fecb33f63a0dca77154a53cce215335dd0e`  
		Last Modified: Mon, 12 Apr 2021 18:22:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132795db2760b73b37339be5f0c1d26bb76a81e6a386921150a111ff850884d4`  
		Last Modified: Mon, 12 Apr 2021 18:22:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f8ed52e47d957d71457cdba7e772563fa99363f726e6f4dff49826409df1e4`  
		Last Modified: Mon, 12 Apr 2021 18:22:01 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009d1aadca7ceb9c986053e925a601ef3081ccd21ec0c51163c19a55a5ab3db2`  
		Last Modified: Mon, 12 Apr 2021 18:22:34 GMT  
		Size: 6.6 MB (6610556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d981ae51eb14502ae86c596f05c17b2a5a0a6f2f779008bb7d3541cc150ae483`  
		Last Modified: Mon, 12 Apr 2021 18:22:33 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941841303ee2334e668b2ec01b802478c97191924072eb87cb1bd8f1ac6830a3`  
		Last Modified: Mon, 12 Apr 2021 18:22:33 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7013ed8e917b4f931811442408535dcf6a7430a2b979f7f26a4bc2a945ad9f8f`  
		Last Modified: Mon, 12 Apr 2021 18:22:33 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9eddc4737aea1b0458b91388dab8b624f89768f35670564b0440f6f0b65a28de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75634316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f892f8aa1730261399b971b20d3b1ac4fd47c117b9c27b2200d882a871b4a4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 12 Apr 2021 18:44:53 GMT
ENV DOCKER_VERSION=20.10.6
# Mon, 12 Apr 2021 18:45:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.6.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 12 Apr 2021 18:45:03 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 12 Apr 2021 18:45:04 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 12 Apr 2021 18:45:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 12 Apr 2021 18:45:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 12 Apr 2021 18:45:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Apr 2021 18:45:09 GMT
CMD ["sh"]
# Mon, 12 Apr 2021 18:45:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 12 Apr 2021 18:45:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 12 Apr 2021 18:45:24 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Mon, 12 Apr 2021 18:45:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 12 Apr 2021 18:45:30 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Mon, 12 Apr 2021 18:45:31 GMT
VOLUME [/var/lib/docker]
# Mon, 12 Apr 2021 18:45:32 GMT
EXPOSE 2375 2376
# Mon, 12 Apr 2021 18:45:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 12 Apr 2021 18:45:34 GMT
CMD []
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a57337189c50d5d385c7f55f4769fd57d0ce57fdf1017da10ab5ec777136e6`  
		Last Modified: Mon, 12 Apr 2021 18:46:44 GMT  
		Size: 64.3 MB (64345292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7018023bb74c64d377be9a28d940dce80703ec96b7a620d79bf1d9ec31d5fd`  
		Last Modified: Mon, 12 Apr 2021 18:46:26 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a8ae0e3e03c9ee5d64a225846771fa00e99899fffaea01fdde025888fb813b`  
		Last Modified: Mon, 12 Apr 2021 18:46:27 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2c9c3f05a88a04abd96b41d3129e8b01395bb166698e5fdda2aef3625c38a9`  
		Last Modified: Mon, 12 Apr 2021 18:46:26 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f2f8b5f5e4167037f268978d9cbdccf10fbd5803e30f6ed0c5be0c28eec1f7`  
		Last Modified: Mon, 12 Apr 2021 18:46:56 GMT  
		Size: 6.5 MB (6512609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ae220ab2a8dd9c1618faf95df4e2296afa78527e94443429263cedaf806fc0`  
		Last Modified: Mon, 12 Apr 2021 18:46:54 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fdd7e48661bffb73543d93b59ca3d02182aaac038b01b2c4c645e089e76d50`  
		Last Modified: Mon, 12 Apr 2021 18:46:55 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8dfd1012c648a414d0089bf37ada989b6cc260976cfc0bc33ffdf0251a46106`  
		Last Modified: Mon, 12 Apr 2021 18:46:55 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
