## `sapmachine:lts-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:aa870f280f51286d0ebe5e174c5f9782d8ac67c528af96fe955f360c652742f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ada266046f6d38c5a9ebf63ad8fccc8b969eb5ce4b35dea4df38cdbe0b52cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85209401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42c0260641623351ad7a1d8d037c27855d6bddea443388706609f4da4a9cef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:38:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3d51bfa88546228a9900a5d72616b886a15a1b2b53cf76c39b939225230143`  
		Last Modified: Thu, 13 Nov 2025 23:38:35 GMT  
		Size: 55.7 MB (55672603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38f2b18b76ab4ad05187b801115aaf238a3661a4845992fd65441b5c248b8544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d19f34ae8b9eb164d5d4c65ccbc48f19f0e708ffb70731279c54b0ce434658e`

```dockerfile
```

-	Layers:
	-	`sha256:42ef326e9647839373bfa87be8d4fc9170d0e1d01266725769775e79db6e290d`  
		Last Modified: Fri, 14 Nov 2025 01:13:28 GMT  
		Size: 2.3 MB (2300655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35778c990725bd0fe62786cbe531b64784826c4513f90ae8061620360f24c983`  
		Last Modified: Fri, 14 Nov 2025 01:13:31 GMT  
		Size: 10.3 KB (10272 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cc7b68a6c0f023ed5cbe424d641573f968c0335d17181c131a570a21b4a3cf23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81945156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e30dddc9bd499bf6a9f308108e3f0289fcf38e2475f4848dd327efada6ad8eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:23 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8159e1ba8c4a0d34c1dfca7922e2270186b490879387989860e41cab308a76e`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 54.6 MB (54561279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:58c55b06c8323cff10bbac1a5252e9d37868a17584ae92247b6afa9d1769413e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1c85b70ef80cf2fa704dacaba11e3d07888efb62a6535c440d7e37fa852107`

```dockerfile
```

-	Layers:
	-	`sha256:6b442566aae8fc0577949a46d47f7e24cfd4e7f2f928411cf125dc17dd7d1d6a`  
		Last Modified: Fri, 14 Nov 2025 01:13:35 GMT  
		Size: 2.3 MB (2300372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:603940e8efc84852cf0eb770e9e98d01e4db65ec00631465708e46eed0f279d4`  
		Last Modified: Fri, 14 Nov 2025 01:13:35 GMT  
		Size: 10.4 KB (10424 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:84dc1abb371f4fb0f4e99783d00e8c683146efde12006af63965e46a2dd8a3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90736827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0321a810c7f2548d87af59f780c98595ad5bf7443b33cf8a3575e0633757088c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:23:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:23:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 14 Nov 2025 01:23:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5d7dcbda8f136b48be360c8a8f4f24704fe92c55988e9f0162db9f87365f9c`  
		Last Modified: Fri, 14 Nov 2025 01:24:37 GMT  
		Size: 56.3 MB (56290105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:734b0669d569efb4dde6d321c30248153df428c18e8e4385b08d853857efe53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f6c2c717c23082520e95a643175e787d86c169fc6b9e646746a70a8c4ebda2`

```dockerfile
```

-	Layers:
	-	`sha256:06730bdc3c29a9f1fc0f3cf9fb0d2f4fa7cba2bee6668aa4b6fed69209a33157`  
		Last Modified: Fri, 14 Nov 2025 04:11:11 GMT  
		Size: 2.3 MB (2298074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23362414b8d165268eaa25ea2c97ee3fc3ce37386ba16b0c72b145cac68f8b22`  
		Last Modified: Fri, 14 Nov 2025 04:11:12 GMT  
		Size: 10.3 KB (10340 bytes)  
		MIME: application/vnd.in-toto+json
