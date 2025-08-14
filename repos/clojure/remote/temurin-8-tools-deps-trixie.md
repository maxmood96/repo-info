## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:0042979d78d16e971d6b1661c0d459dc7ffe13d98d452921e32722fba80b4399
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6d0d8d90e46102014bdb4caa2acaa0e8c2040f52068c9fcb00003f936cfb2eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189396297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fd84c15b145d9bf96305b18e0e95faf8a5ba0c650104cdaf7f4bf8b7754f0`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc1fd05587ed0c4c0541e56188dc5d2ce0921cc5a956edac9da6205d70cff51`  
		Last Modified: Tue, 12 Aug 2025 21:34:46 GMT  
		Size: 54.7 MB (54731348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bbe07b984b5a5def421d7b558cb12898bf5a55ccab1a6dc02911a4e97c1c3c`  
		Last Modified: Tue, 12 Aug 2025 21:35:10 GMT  
		Size: 85.4 MB (85386026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1ba6d5b1f0d8590f022e30e7e109ce4c1f5a95b35ee39e338dfb92ee179fcc`  
		Last Modified: Tue, 12 Aug 2025 21:34:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:76c0aff455e156f74ecd9fd747cb31e870ce2823de143e251642f77ec4fceebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d5e1929627b8dd56c01543c590751353ec59d8f5aeb94c6bd8bedcbe7372e0`

```dockerfile
```

-	Layers:
	-	`sha256:783f6da1132e4c1019ff1e299cdbc51ca923cbf61a731a1f4831fbe933c52bf2`  
		Last Modified: Wed, 13 Aug 2025 00:42:35 GMT  
		Size: 7.6 MB (7583802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35c1cce0f184cc4dddae73e0a18518590a4df0c995bc6d1c1cdb067f32e11ea1`  
		Last Modified: Wed, 13 Aug 2025 00:42:36 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:80b283d912f6238cf7ae17ce63269b466ea9b62e16f9e530e54d7b11945f224b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188688545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b082d2155ea2b83a61c881fc4b75ba95cf2f1aa33a0584abbd2913e1695a44c`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9627aac89a9847aae2591b09306769bf8d0aec6e6f183e8e1dd66f46934035f3`  
		Last Modified: Wed, 13 Aug 2025 14:05:17 GMT  
		Size: 53.8 MB (53835638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b191b1c7441a90aa16015b6c2bbf479a63303a3235abef3d69d106eef6b49831`  
		Last Modified: Wed, 13 Aug 2025 14:08:53 GMT  
		Size: 85.2 MB (85210661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d61bde911c290926ba438e3a6ce24af907bb21c5156613dcfa33d745cd99fe`  
		Last Modified: Wed, 13 Aug 2025 14:49:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f543a297f78d46306f08ed834eabb6d36bb640c0f6e4fc45e5fb504d506f00d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9764413c0e0c51b88da65e48eb0ad06b38b1c8029d11ed346a95e8a44a9ca05`

```dockerfile
```

-	Layers:
	-	`sha256:c506ccfe9713c45dd52486208e95aebb70ecd3d9c67b0366b2cfa9ed226908c7`  
		Last Modified: Wed, 13 Aug 2025 15:43:21 GMT  
		Size: 7.6 MB (7591530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ddd11eb77045547fb1b833f60fe712293a90c621325cf75e4dabbee45806b2f`  
		Last Modified: Wed, 13 Aug 2025 15:43:22 GMT  
		Size: 14.3 KB (14330 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2e623ad6a5643e54092df449a6b45182168a88ebcfabf9138d5a08efcc906e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196064463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706ea0b6897635050ec2e94a5ac62eb3f231ccb74b78cc5147ba739af38d7158`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9952392f1d63a20569b12f965f2751bde5df8daa145796a1c86ef6a956fa67d8`  
		Last Modified: Wed, 13 Aug 2025 19:21:30 GMT  
		Size: 52.2 MB (52165399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b4791dadc00011c9eef9470bc92c9e0d6e591254065befc7c769ab730b9311`  
		Last Modified: Wed, 13 Aug 2025 19:27:54 GMT  
		Size: 90.8 MB (90795035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51db5c9631599907f7869c06b08aa7500bc094b68c6c7af5d08b77de478e92f3`  
		Last Modified: Wed, 13 Aug 2025 19:35:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1cccf6e3b7667c90754525b18e1d786372758bff28a401c1cabc90694ac548e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3029a2ba045132da6729307df119f28e4b4cac3511773fd5c9c249e1afe030b`

```dockerfile
```

-	Layers:
	-	`sha256:9e0efb1804a33284fc8faa605feebd13c0c3263accfaa9c239643153fc9500b5`  
		Last Modified: Wed, 13 Aug 2025 21:41:15 GMT  
		Size: 7.6 MB (7588814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e2819e6b74f330b244635de2ed81fa764a76f3b11f39daab0f9e85b5dbb073`  
		Last Modified: Wed, 13 Aug 2025 21:41:16 GMT  
		Size: 14.3 KB (14260 bytes)  
		MIME: application/vnd.in-toto+json
