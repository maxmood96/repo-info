## `sapmachine:21-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:66867740d64b052ba338812f42c9cd88d2775944eef4ead67f4736e4069d0eb2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:9e2d7d9f12448f8ba870a49b8421c640c9adfcab84e1b154dd214592b2c678b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245032666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747a19c827bd8ac9a9d674b95dfd862facdc15446e0c5156354a7778824c48ae`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b14c2b54901abfd359490c47d35146492e634f7ad15a2cfb32653fda2b2da9`  
		Last Modified: Tue, 02 Sep 2025 01:13:42 GMT  
		Size: 215.3 MB (215309602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d56c135d0d592642599e4ddab92d15ef946519059deeb192eb11818cb31bb1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd6ec4acd90528713434c996a5d00c039db51bd805e75032f8acae6cb0b779e`

```dockerfile
```

-	Layers:
	-	`sha256:6cfefce08a528591cc1a6d682f9ba763f0006eb0949c38caaa4485634495c549`  
		Last Modified: Tue, 02 Sep 2025 03:07:08 GMT  
		Size: 2.6 MB (2606953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32dbc6ba53f4b1bf885ca986c2ae6640ca90b164abe4f321b02a10a34a3e941b`  
		Last Modified: Tue, 02 Sep 2025 03:07:09 GMT  
		Size: 14.9 KB (14885 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d7793f2cc8475d3a0532db354428aa8ac1b4b4bfb1213672d5575aff3ed0cf0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242406639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276913a3e5259549839a4d7f8e7411046fbce5ef37692acf6364ebf0f083eeac`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124ee7cdc81cdb75b3c313baff024da00a67dd4cfb304a7708f8ff9f197ab073`  
		Last Modified: Tue, 02 Sep 2025 03:05:47 GMT  
		Size: 213.5 MB (213546399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ffa84262555cf75735f33fc6b2b2a96958b503059576ccafb2b188a469833f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054d80a6e98879d8910d00871baeb21d535ff4d997bd830cb2b9b6031d8a5626`

```dockerfile
```

-	Layers:
	-	`sha256:d44aeddba949c192c4a86e97c4c1a3cebbf9868d64a8245738cc1ef45f9cea91`  
		Last Modified: Tue, 02 Sep 2025 06:06:26 GMT  
		Size: 2.6 MB (2607649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eba28b4109197ec4722e9e216e94f737a586b5b41ee3053843552bbf16d7de8`  
		Last Modified: Tue, 02 Sep 2025 06:06:27 GMT  
		Size: 15.2 KB (15215 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:63751a4b216dff6d5d9f93c005479a63f09989ff70f283deb22796943afb1f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250593532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559297c530dcd2156afd7c9095edcb6bd830d74a5829a4c398b5d4066234d36c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110505d30f9d2a804b70954ece15e95c10049c25bdf4a800289377442f481ca8`  
		Last Modified: Tue, 02 Sep 2025 02:01:38 GMT  
		Size: 216.3 MB (216263999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cfb88ba3abc50c15c0d31840d5081b68413414228c2e15b8cf74652ad61f09a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7a8cf2ba847106788e866a890b07e3443781a969c1039c248fa77d0501aaaf`

```dockerfile
```

-	Layers:
	-	`sha256:afa7fc63a46d72d028db9ab60907eefa804e3e85fe236c1b8191df9fbd7f6f39`  
		Last Modified: Tue, 02 Sep 2025 03:07:16 GMT  
		Size: 2.6 MB (2603178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6180fbfb9a565ed0fd43b47cb9a9226d6093eb9934b9307571e178d695de8e`  
		Last Modified: Tue, 02 Sep 2025 03:07:17 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json
