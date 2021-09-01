## `docker:dind-rootless`

```console
$ docker pull docker@sha256:5fc0a5557f592318c88170dc504b206e94ab12c3163abc029b7e070e837d7810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:33a0761966c87569be2a9763c8c477dd3e8981982c8abc4324c090f9d2478231
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92930272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5357717b590217cbd992209ed6e2fb34e8ba65a74d3a5324c9b916395a15cb1b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:26:39 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 00:26:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:26:40 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 00:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 00:26:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 00:26:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 00:26:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:48 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 00:26:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 00:26:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:26:55 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 00:26:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 00:26:57 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 00:26:57 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 00:26:57 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 00:26:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 00:26:58 GMT
CMD []
# Wed, 01 Sep 2021 00:27:03 GMT
RUN apk add --no-cache iproute2
# Wed, 01 Sep 2021 00:27:03 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 01 Sep 2021 00:27:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 01 Sep 2021 00:27:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 01 Sep 2021 00:27:07 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 01 Sep 2021 00:27:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 01 Sep 2021 00:27:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de31523ae09475f6d68e873b416f497c2bd9a92224d9dc9224e1ec4c0a6066e`  
		Last Modified: Wed, 01 Sep 2021 00:27:41 GMT  
		Size: 2.1 MB (2051151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3856ddc4bf6a58ca53ceb6444141995979c00718b20dae8c849231fcf9bfae27`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117e19917ef5839774785d348adb2ff996bccac5f12d461ca21ecfd58283314`  
		Last Modified: Wed, 01 Sep 2021 00:27:51 GMT  
		Size: 61.3 MB (61284048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53eeb058f8c3c25c5b9f9d12769ab386c353b9f48506daae8fdebd88a33a21`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223565313e3813eda94fc3641a51cdd88a37775e7b9817ada2a57bd45050906`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa82c493f72cf1d33f4a0bd90320bdb1923957f3cb3b0d36596f52bad68ecb4`  
		Last Modified: Wed, 01 Sep 2021 00:27:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5973cffe69ed6ec4ab2e2a3a191794cfba7339588cdbc4f3c6355e040c05fb`  
		Last Modified: Wed, 01 Sep 2021 00:28:13 GMT  
		Size: 6.5 MB (6524532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a47d00d0a33090100f0be8b5d564e20357fa60a275aba922aea6db6fb47531`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8a29d06b5993e5468f57fa6a9d0adff807919d6c664b785a96b1fb6a96d8`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 978.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6762b64189d2495a0856c3f7d465d7ad0f91a4e2db42b4093e70c7b55e571211`  
		Last Modified: Wed, 01 Sep 2021 00:28:11 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dbc14ca68582d0028413d0826f71ced2423d092126de153c91bbf05e4c98fa`  
		Last Modified: Wed, 01 Sep 2021 00:28:35 GMT  
		Size: 1.1 MB (1131899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2498ce93d923f17fb67004858df28e840d729cf6e6fbdfa82ed3c82679ebe4`  
		Last Modified: Wed, 01 Sep 2021 00:28:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64015873fa22ddcd58c65fa437669d9153f1a1fd72fd3a43dbd6873f129461b9`  
		Last Modified: Wed, 01 Sep 2021 00:28:35 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcf73021c4287b49de963988902f36818158f72e0ccd6e3b93af6bb3f4e7ef9`  
		Last Modified: Wed, 01 Sep 2021 00:28:39 GMT  
		Size: 19.1 MB (19116093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57ea275b05bd4bf7a61d8bc934c3d72b3d30ae866ed920fdd7d0a5d06933c0d`  
		Last Modified: Wed, 01 Sep 2021 00:28:34 GMT  
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
