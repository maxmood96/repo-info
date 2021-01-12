## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:d745f6f5f9bf25f25c901bb47baa36ea40691e638ec6bd4107759ed793de666b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f2cf008f1ddd730327a1adf52056c80c6797f6d79dc3c6036a3b7cfc08527cc6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110582633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304733fb42d340d5539d864fdca63b075d5af6940044cc9ecf6bf1d5c8cb2904`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 17:01:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 17:01:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 17:01:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072739d44e4fe2316d3bda5b6e0944796b1824cb2dee521ef06bf11e4f5db0fe`  
		Last Modified: Thu, 17 Dec 2020 17:27:45 GMT  
		Size: 10.8 MB (10752737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5111f27e9600a1fa0a3a8660e8518294729a41abcd648bbf0ec9f60dcfb02b73`  
		Last Modified: Thu, 17 Dec 2020 17:27:45 GMT  
		Size: 4.3 MB (4340690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc22afea6082f2878516aa02ac2285e9f35c880c32e2c0dc6879756d9dcce23f`  
		Last Modified: Thu, 17 Dec 2020 17:28:05 GMT  
		Size: 50.1 MB (50111600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b37f382bdcc9addf9c484ad69862f57bc16ea7500c07b88f1f218b8747fb1e20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106381551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92d9b135dfa9f58b11ac073d7bf187cbccc43064e3b3bed13d6e5a02a011ff8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:55:15 GMT
ADD file:3047f832191e46ed288c3efd5d017316fc7b7d8fbd282800d02da8ca0f799430 in / 
# Tue, 12 Jan 2021 00:55:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:37:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:37:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c99253078aee5285b1d9437ad45736eccc40de8b1007a23b3de45924452cfb0d`  
		Last Modified: Tue, 12 Jan 2021 01:04:44 GMT  
		Size: 44.1 MB (44091438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8cd662e395616851748f77d200cebcd23c0ff3e1416b086bba54350bdacea9`  
		Last Modified: Tue, 12 Jan 2021 01:47:15 GMT  
		Size: 9.8 MB (9827084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae70193a410fd3620313dc1177f88c9edcea3db4659c8d9da8294f29939e21`  
		Last Modified: Tue, 12 Jan 2021 01:47:14 GMT  
		Size: 4.2 MB (4160279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b82525c1b286ca16c60a4769d1d318c6e2555de48b58e90c951421088d3627`  
		Last Modified: Tue, 12 Jan 2021 01:47:45 GMT  
		Size: 48.3 MB (48302750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1d1a3960456783bafab1d51197bc6a47d2bec67820264c731de04f999f4981ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101899357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e2f265baa94edc78144aaeaa96b79ea9051eb2c7d0b37962dae7da24977ac6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:05:19 GMT
ADD file:9c744a203d36aa8c515bbc11873a4a479cdf3fe9f020ca1ef207b53e6b3a251e in / 
# Tue, 12 Jan 2021 00:05:23 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:21:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:22:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f5de2649c1cd9091872f81b8ceb6a67890124f113d9fce9c52bf60d5a6e19f43`  
		Last Modified: Tue, 12 Jan 2021 00:15:23 GMT  
		Size: 42.1 MB (42119951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cae60aac6e598935e2b14216dc4265434ba03d17c82f622b18abb712577d2c`  
		Last Modified: Tue, 12 Jan 2021 01:34:01 GMT  
		Size: 9.4 MB (9446203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9694e28a75917ff08caeaee5ed8729a2f12d2110bf203781d578006a0ef2f7`  
		Last Modified: Tue, 12 Jan 2021 01:33:59 GMT  
		Size: 3.9 MB (3919958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49da7baaa533b2272938593647e65b46d3fd7a5df2211e746229f18c95ea81fb`  
		Last Modified: Tue, 12 Jan 2021 01:34:27 GMT  
		Size: 46.4 MB (46413245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:eaad05de54581d05b7d6fbf0eadf3eb554691bf79507b72fcf1faab4d70a0981
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105020674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e0aabaa0dc1841b1bafcc9bb5638ecd8a24b7a2b218e973f2ca38eb853b3f4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:45:18 GMT
ADD file:bc4af94773a01defa7a79adb22199dde2229843dae224d13d3385c522cb71652 in / 
# Tue, 12 Jan 2021 00:45:22 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:30:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:30:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:31:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec4f0a0f30ab1b4fc2e412a926b8608502de98203ca1994c7916de2017136729`  
		Last Modified: Tue, 12 Jan 2021 00:54:45 GMT  
		Size: 43.2 MB (43177964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0d21e1234248b5afd95bc41f061ec505353daeca6d4d5312a0167507857e72`  
		Last Modified: Tue, 12 Jan 2021 01:41:51 GMT  
		Size: 9.7 MB (9703645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e47f4b9ead7d5e8caca5072922207d5aa928f0144af32c78cf5a7e165f1898b`  
		Last Modified: Tue, 12 Jan 2021 01:41:48 GMT  
		Size: 4.1 MB (4095462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12669d76f10697ce6f8db3816f905c864edac1edb9ff9264a5c77c52e93e970`  
		Last Modified: Tue, 12 Jan 2021 01:42:16 GMT  
		Size: 48.0 MB (48043603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d5fc133210e64b228576205f9ca83f7d50bcf219d24af5207e5586f58d262467
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113060963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067277f4c0252ff1dff6f65870235b333fe61076889b6c59648d818c727f6b3a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:38 GMT
ADD file:65da710638e196cb40b07b1d2461114bb3c8b34d69693449a905397c192f1ac0 in / 
# Fri, 11 Dec 2020 02:05:38 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:12:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 08:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6c30bba175680710c6b02f65235cc2a0b8adf1ec4be1e440e260afda9487b37`  
		Last Modified: Fri, 11 Dec 2020 02:13:22 GMT  
		Size: 46.1 MB (46095117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc0247c6906d18f48f42d4ecdf060009453e884a50dba3d3b52166e5bd61ded`  
		Last Modified: Thu, 17 Dec 2020 08:29:18 GMT  
		Size: 10.8 MB (10774964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75bcca64ffc98da2fb811c456d5ab074caf61174cb723eb8429a5e4ade473a4`  
		Last Modified: Thu, 17 Dec 2020 08:29:15 GMT  
		Size: 4.6 MB (4563306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2949e32cf476c215c8b8ec60ce8dfdf335001f253da3619f69e3bbc6566ade`  
		Last Modified: Thu, 17 Dec 2020 08:29:43 GMT  
		Size: 51.6 MB (51627576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
