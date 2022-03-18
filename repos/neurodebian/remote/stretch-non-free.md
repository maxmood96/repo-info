## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:b519907c1c159c34e0e8019a6b75aa1194a0eecbe5916794d7dd3e9383d5275f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:565b9ea4f0645a44b0738ff3956adb05e176ab38a137fd49a8811f441b16b186
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52296443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77669f19123e9ed2f887485717b627f8182eaff8551b84ff614303db87becdc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:37 GMT
ADD file:0d1703dd365e8d6f8625b40addc388cab8f0423af2bca03b0baea5d27f585a9c in / 
# Thu, 17 Mar 2022 04:06:37 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:13:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:13:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:13:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:00 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d172ccdc78ea7d453ae5fa3feafee94e3837e6f8e282d8501e668329c49551ed`  
		Last Modified: Thu, 17 Mar 2022 04:13:38 GMT  
		Size: 45.4 MB (45427778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be042bfa7a0b55e2682cd3788568190ac9be01e50fa1b6cf821dc4e6a947c75d`  
		Last Modified: Fri, 18 Mar 2022 08:17:11 GMT  
		Size: 6.6 MB (6572658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c261c726a69dfb82b29305d696a5f9f9f2e8eb82a894e5219b96687d1227a6`  
		Last Modified: Fri, 18 Mar 2022 08:17:10 GMT  
		Size: 3.2 KB (3159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b6863580e6fd41b0211773626ac34742647f168e91152dda28aa3fcfdce666`  
		Last Modified: Fri, 18 Mar 2022 08:17:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76abd5f1f23cc1325465778afc3d7cb8517fad26d4eda5715c3a9fdb2df4d1d8`  
		Last Modified: Fri, 18 Mar 2022 08:17:11 GMT  
		Size: 292.2 KB (292240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719897ab8fcba86f33284aac6712bae782b28ace5211fa00f84ddc03d6f3f4fa`  
		Last Modified: Fri, 18 Mar 2022 08:17:27 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
