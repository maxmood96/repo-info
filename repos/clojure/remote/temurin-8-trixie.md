## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:acef7a525fa7130ae4c5e98c5707e8c577ec07a1ade68d49a3bc17df1b352074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:0fb7a96cdf87bbf957b198fff8a8ef1af628362112d6c87211526b8caf67861d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190043907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33111361aa176a6891339282c30859e2b3987b8f12de5d3ea9aaab8b7a16213f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:14:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:14:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:14:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:14:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:14:53 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:15:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:15:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:15:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5af1ac54abea44489149d0792f3bdb33eb1891d419d5755ebafc1a5570ec0e`  
		Last Modified: Fri, 08 May 2026 20:15:31 GMT  
		Size: 55.2 MB (55170047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfb9ec453ad9fce5e386ceb439c385b78fc7e89bf6e7e7072cf63f8463ea87b`  
		Last Modified: Fri, 08 May 2026 20:15:32 GMT  
		Size: 85.6 MB (85570894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d38bd49c2128568efc82447aa1d74d431c9f026dff48cba059107b0884c6ed5`  
		Last Modified: Fri, 08 May 2026 20:15:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:35f6f077abeaa2276a244d86dcdcaea7f991186d11a74f9d73eb0d8d48aa91b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc57a6b03ecacd53ce7e781d2f2a1215a80e82119037c1fe8c7cdf83a077f4db`

```dockerfile
```

-	Layers:
	-	`sha256:3d87afcdb5ab01a5603e7d0ce900574ce5f28a1d4d4bf2fcf17a78c8c24fcc78`  
		Last Modified: Fri, 08 May 2026 20:15:29 GMT  
		Size: 7.6 MB (7591708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81450393c1b66e5b1ec063c0bf5bc73f5c6e60eebdc1d454e2ca0ab555d39fdb`  
		Last Modified: Fri, 08 May 2026 20:15:29 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ef398f55990f2e7a6b8591e575f8bed59bbc120e34416e5495681b85d38fe05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189305184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdf07bb6f46804cb7612a6c4bc48455933e0508559733cb334fe3fa0200c770`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:19:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:19:26 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:19:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:19:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc265bf70c13a606de0fd82f58b335e7eb05258a5601566f49289756b7e0a0d6`  
		Last Modified: Fri, 08 May 2026 20:20:04 GMT  
		Size: 54.3 MB (54251628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fce7992a8adfba8c8992017574a12180b3381579f596f69223c50ed4339ee`  
		Last Modified: Fri, 08 May 2026 20:20:05 GMT  
		Size: 85.4 MB (85383465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0e03fbdd331895c3e837b3d1aefca6c289a31dc3f8f8544df47b1dafe45df2`  
		Last Modified: Fri, 08 May 2026 20:20:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4a52273d0d34c0b67772c257faa00ae66b24d0e9e50de415698d65926747d75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6562e1f6d8479b5d5aaa2ed28a35e32d24a05213bb01ac26e4598f309a51c02c`

```dockerfile
```

-	Layers:
	-	`sha256:aadfcbc315d0fb3e766931717b07721acb466ab6f0057d041072fa3914bfadfa`  
		Last Modified: Fri, 08 May 2026 20:20:02 GMT  
		Size: 7.6 MB (7599438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0d1db8406b4c8399e3857686c402d5611ab1b6ece9e9f7d53386f1a13cf30bf`  
		Last Modified: Fri, 08 May 2026 20:20:01 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c0bb1194679eb58a2873511409766001b7aa9e111a8a3e76b8dfe0bdb7be3f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196760402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2fdb3a35a2099c97a825161cfa27ebe47e985b9c3a9fc09996083202202220`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:15:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:15:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:15:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:15:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:15:39 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:19:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:19:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:19:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40946bd06af436e9aec289d6d571e7a23a7c73218795b260867e8f81c9497e46`  
		Last Modified: Wed, 22 Apr 2026 08:16:57 GMT  
		Size: 52.7 MB (52650392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f41aab2e5d97f15ed30df40d0f5927cadec923366c2a60df9cc18d89760cd4d`  
		Last Modified: Wed, 22 Apr 2026 08:20:16 GMT  
		Size: 91.0 MB (90986382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d392a99dc148a2cc6dbea9062469749b22555f9f1a29364fca67309bb4dffbf0`  
		Last Modified: Wed, 22 Apr 2026 08:20:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:76e32adcda3bbfb08c74137175e3eb7de2b0e33b012a544ca1196efbbf93bb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326993c409c226fab0563ddb649e59eed12123af211c2d2df991c3f55301496b`

```dockerfile
```

-	Layers:
	-	`sha256:7512f265e1d7318fe3f7324787565736fcacc2cb4889b157e84a090327779bd6`  
		Last Modified: Wed, 22 Apr 2026 08:20:14 GMT  
		Size: 7.6 MB (7596724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082f19142c58cd0b97133531fc918473e88f547b1a8bf319ab45d950a3fe74c4`  
		Last Modified: Wed, 22 Apr 2026 08:20:13 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
