## `docker:dind-rootless`

```console
$ docker pull docker@sha256:963579745bca14f3cbd0d13ccc9b1909864e735d180c585ec47aa1f7d2257fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:124b738e215234286634752adb38a03fca0b5f4d46c291a1f77a84b0383a1e5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93315315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7347a3756263d56fd413c805bf0cb3bc52910009c4dbc12a4c8e84ba4359ffe6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 04 Aug 2021 21:20:35 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 04 Aug 2021 21:20:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 04 Aug 2021 21:20:36 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 04 Aug 2021 21:20:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 04 Aug 2021 21:20:43 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 04 Aug 2021 21:20:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 04 Aug 2021 21:20:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 04 Aug 2021 21:20:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 04 Aug 2021 21:20:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Aug 2021 21:20:44 GMT
CMD ["sh"]
# Wed, 04 Aug 2021 21:20:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 04 Aug 2021 21:20:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 04 Aug 2021 21:20:51 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 04 Aug 2021 21:20:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 04 Aug 2021 21:20:52 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 04 Aug 2021 21:20:52 GMT
VOLUME [/var/lib/docker]
# Wed, 04 Aug 2021 21:20:52 GMT
EXPOSE 2375 2376
# Wed, 04 Aug 2021 21:20:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 04 Aug 2021 21:20:53 GMT
CMD []
# Wed, 04 Aug 2021 21:20:57 GMT
RUN apk add --no-cache iproute2
# Wed, 04 Aug 2021 21:20:58 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 04 Aug 2021 21:20:58 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 04 Aug 2021 21:21:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 04 Aug 2021 21:21:01 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 04 Aug 2021 21:21:01 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 04 Aug 2021 21:21:01 GMT
USER rootless
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b94fafbd542a8c279f4a08e81fef317862b0fe3f604febe2fc2138886ba1d7`  
		Last Modified: Wed, 04 Aug 2021 21:21:53 GMT  
		Size: 2.4 MB (2438245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e3c9e6c132861fd24ac22906718bb610ebcf3912ade5e48a791ba8f85e5799`  
		Last Modified: Wed, 04 Aug 2021 21:21:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc990f87bf12a7b8fb86c3003977468a14fb1a31e5bb0b500e8127ee4e6beb5`  
		Last Modified: Wed, 04 Aug 2021 21:22:03 GMT  
		Size: 61.3 MB (61284061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1436504743cc47a166b7964d591792b69e34aa1e3e07ef5d91f481fdb11f948d`  
		Last Modified: Wed, 04 Aug 2021 21:21:51 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c526f01240b836e9645a2b2b629051c5e488d60b309d5f253adab7f2c45ed7`  
		Last Modified: Wed, 04 Aug 2021 21:21:50 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d263b0ed3ea3116c812ca5c542c5175ccb0c99bee76b06db8c2340290057fa`  
		Last Modified: Wed, 04 Aug 2021 21:21:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323e02cdc2f5b38baeff0de98fb35ef0d98c8eb6ee03c82bad90c145c7fe31a5`  
		Last Modified: Wed, 04 Aug 2021 21:22:21 GMT  
		Size: 6.5 MB (6524551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278c396f7286d8283a874d8792049d325633fac7e850531740d22f560c955187`  
		Last Modified: Wed, 04 Aug 2021 21:22:20 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8ecf0198691794c5ecaa8389e5beef5e882d6cfec101c6a09dd9ace85ab594`  
		Last Modified: Wed, 04 Aug 2021 21:22:20 GMT  
		Size: 979.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662824727357b53a9d351903bfd330007c20c9576b971e2a06c0018226c6c3b`  
		Last Modified: Wed, 04 Aug 2021 21:22:20 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e6256c33c0ede1adebf65b20431decf86e9ee5ee75bc5dafdc97323eb00b14`  
		Last Modified: Wed, 04 Aug 2021 21:22:39 GMT  
		Size: 1.1 MB (1131912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ee6cc75d0fb6ad7733a1aff3c28f0f3f7e0b2fab5a6a3834b15f4448fafd63`  
		Last Modified: Wed, 04 Aug 2021 21:22:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53de6cbf547b0318998261b99b7a0a30bd3fcde67956de7983df1b2328af358`  
		Last Modified: Wed, 04 Aug 2021 21:22:39 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956907e972957db3a2ae0b2ea1caad912dbfeb36651f885dd48cd155e666de43`  
		Last Modified: Wed, 04 Aug 2021 21:22:42 GMT  
		Size: 19.1 MB (19116096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39800d8bc1636f365b4faf120564b96243d4c0cb880f893e9b561a609f4758d1`  
		Last Modified: Wed, 04 Aug 2021 21:22:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8798010c693f3e0ab32e9c78938345734472925bde322d6eb50d015729da5738
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89262967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796d21eeac11e41216052d96f3f42968c38bd60d22c93a28c08f5c8b0adb6510`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Wed, 04 Aug 2021 21:40:35 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 04 Aug 2021 21:40:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 04 Aug 2021 21:40:35 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 04 Aug 2021 21:40:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 04 Aug 2021 21:40:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 04 Aug 2021 21:40:39 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 04 Aug 2021 21:40:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 04 Aug 2021 21:40:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 04 Aug 2021 21:40:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Aug 2021 21:40:41 GMT
CMD ["sh"]
# Wed, 04 Aug 2021 21:40:49 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 04 Aug 2021 21:40:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 04 Aug 2021 21:40:50 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 04 Aug 2021 21:40:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 04 Aug 2021 21:40:51 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 04 Aug 2021 21:40:52 GMT
VOLUME [/var/lib/docker]
# Wed, 04 Aug 2021 21:40:52 GMT
EXPOSE 2375 2376
# Wed, 04 Aug 2021 21:40:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 04 Aug 2021 21:40:52 GMT
CMD []
# Wed, 04 Aug 2021 21:40:59 GMT
RUN apk add --no-cache iproute2
# Wed, 04 Aug 2021 21:41:00 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 04 Aug 2021 21:41:01 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 04 Aug 2021 21:41:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 04 Aug 2021 21:41:04 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 04 Aug 2021 21:41:04 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 04 Aug 2021 21:41:04 GMT
USER rootless
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d668eead8965ee8f4a1cd65de2a1cde9c49cfd2c2f06ac2290e0b90724ba4ea3`  
		Last Modified: Wed, 04 Aug 2021 21:42:32 GMT  
		Size: 2.5 MB (2458333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7010a04da6233aa993b677900fe12554cb30e4b12adeee36a2c884d5c0ec8965`  
		Last Modified: Wed, 04 Aug 2021 21:42:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c06e26407aeefb6fd4953cb12e19c70695281c4c9ab4e9b8120734669094a8a`  
		Last Modified: Wed, 04 Aug 2021 21:42:39 GMT  
		Size: 55.4 MB (55420354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674e4b73ac390f4f52af96ffa7e98228c80619fa25bd61e862485f64b509a849`  
		Last Modified: Wed, 04 Aug 2021 21:42:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627ac7844e75fc94ea8963915c871cb5e376af3631da0ce14bf5a5662813175f`  
		Last Modified: Wed, 04 Aug 2021 21:42:29 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be33fcd733ebf68f8983483238e2245237efdc7751c83d98e9ce9b6a0f3069f`  
		Last Modified: Wed, 04 Aug 2021 21:42:29 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7be703642618a8d45d2234fbab8868b1139a87c1d15e9ed461b84c174d6a50`  
		Last Modified: Wed, 04 Aug 2021 21:42:59 GMT  
		Size: 6.4 MB (6415768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d505b30c548b9339cb05141edaeeb535a1f6957a797abe632d52f98cc323a97`  
		Last Modified: Wed, 04 Aug 2021 21:42:58 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4a4ed41a0a4416dc51a066b9e02ee59d31136060b4b70de974046278cbaf0f`  
		Last Modified: Wed, 04 Aug 2021 21:42:59 GMT  
		Size: 975.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88540cd1423a8caeac6757a720ddc1be1455af90c51f8242cc0039ca1f5d3b37`  
		Last Modified: Wed, 04 Aug 2021 21:42:58 GMT  
		Size: 2.6 KB (2615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca55d719f285c206e9d9b9f065be06c1921f50cd25f3410d55d34ef73917dcb8`  
		Last Modified: Wed, 04 Aug 2021 21:43:19 GMT  
		Size: 1.2 MB (1153199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af474eb81075318d6a880fdd4d20b5cd59cb8953dc8bdd3e0abee2d3f098d6cc`  
		Last Modified: Wed, 04 Aug 2021 21:43:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8c6d1e64a80e62654c56d0e7179e03154215e4d3a994c2986a5df58e4058df`  
		Last Modified: Wed, 04 Aug 2021 21:43:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39408337edbf619576a8236fe50df4b7600b1a2a69ff501d52acad3a4f3b5a07`  
		Last Modified: Wed, 04 Aug 2021 21:43:24 GMT  
		Size: 21.1 MB (21094815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9ccbcf888a167c7709e18d6a5636d0b5b1e7dbc0f476ae4f25a78642e923e2`  
		Last Modified: Wed, 04 Aug 2021 21:43:18 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
