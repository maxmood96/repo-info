## `sapmachine:17-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:285a01f1a1b17f67bea19481bac49d34a506aaf4b6f5f107317940b84974b71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:c9f0920d4ddcf18c1fc390a14df1985852f660750e53f88c8d752e2c24e281e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229817319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e85cbf479dd7b0772c1eadf858576ab58d0bc760000870a09a9f103f1adcbca`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:44:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 22:44:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c146e02688d406da4511b9e0220df116fca73a7ed7cb4a18cb053a47a9bbf48`  
		Last Modified: Thu, 15 Jan 2026 22:45:50 GMT  
		Size: 200.3 MB (200280652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f7d64138a9536f6959b3339bde2637c17afda40cf48824580fb19455ff792a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8624d60ee7f20739b6858988616ef4d16270dafad2ccf521dc11256b0721d4`

```dockerfile
```

-	Layers:
	-	`sha256:6f2b25fb17bb05d8d5c28fff5dfbb44cae57b23695486b94caed64e8afa7a61b`  
		Last Modified: Thu, 15 Jan 2026 22:45:16 GMT  
		Size: 2.6 MB (2627875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343b99dd54cbd061d45b77439f736c7632595ee118ed1bd029bdc903266983bb`  
		Last Modified: Fri, 16 Jan 2026 01:08:27 GMT  
		Size: 10.1 KB (10095 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c6ddde842505defd9aea9d8d6e0eaf2ecf33028a564b31f15d7393a1f85b45b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226337342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4338b2afed01d597b324e39989a6224b0d1895d4c17822c1ec1261137f5e11`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:48:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:48:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 22:48:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee570f31bcdf79d899939b319e0cebbab2c0ef0150206b44315bad40e63f1be3`  
		Last Modified: Thu, 15 Jan 2026 22:48:58 GMT  
		Size: 199.0 MB (198953845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bae73b14fe3b444cfb2f897cc4a7712a15f548bec3596e8d3a5b77c78795e811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd42c4a0b0f63180bf06070e71e461c7445f7711f6fc7838b30c113657fbec32`

```dockerfile
```

-	Layers:
	-	`sha256:d50007c2e607481634be28226ac185cf8e4f90d60c950c4ba00360579a0bb4e6`  
		Last Modified: Fri, 16 Jan 2026 01:08:32 GMT  
		Size: 2.6 MB (2627605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79b8f637291ce9624432522e258d6dc3d080480b72e5a12865e641e574626b32`  
		Last Modified: Thu, 15 Jan 2026 22:48:54 GMT  
		Size: 10.2 KB (10247 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fab5ca2c5cfe7ac1e0085a4c01fdab2253517d196d77d74ff8906168e0740cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235413005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d23c2674dd763f65797952dea0f3ca3688c39903f7b64ee8b7256e5d4d6f57`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:46:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:46:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 23:46:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e8904e2c6f7553948ccb9fd0c000b60306855b95430d4e1552fb7d938e56f9`  
		Last Modified: Thu, 15 Jan 2026 23:47:37 GMT  
		Size: 201.0 MB (200966043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8edf020b2fc317c852d62afba6471e3375fb86593d1d500f80794b5a2fbf5a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86178b6f9d1eb183220baba1bac0f17d3dd2e8f3beef5be190a319a23e85c1dc`

```dockerfile
```

-	Layers:
	-	`sha256:5fc9a9113c621a667d5cfeaa2cef6fd8823e1eee2cbe44297369f12429fb5531`  
		Last Modified: Fri, 16 Jan 2026 01:08:37 GMT  
		Size: 2.6 MB (2624068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b9a79932ceab0be65880958ac0f3b1d7caa9a47630ae948c84b6304745dcfd`  
		Last Modified: Thu, 15 Jan 2026 23:47:10 GMT  
		Size: 10.2 KB (10162 bytes)  
		MIME: application/vnd.in-toto+json
