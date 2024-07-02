## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:38e562cbec99b5fa104f0cf728d20955704fb24501b103eeed0f210855ec92a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:14d15be151495ba639afbd724c2c9ef28d8fe251fa531916f2402f474c96278a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227703437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4e1e32f676edf84ae4dc6736070246d07f651f4d47ffdac389f9fc9377d3e8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1060fe484d998fb45c544721d5723bdf5c8ad35a7ced0b9140ab6f0d1a565519`  
		Last Modified: Tue, 02 Jul 2024 07:07:00 GMT  
		Size: 103.6 MB (103600210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0228f5f71a86981bb0e3fdaeda118d866150feb744a384c59703462402377cba`  
		Last Modified: Tue, 02 Jul 2024 07:06:59 GMT  
		Size: 69.0 MB (69021222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce31cefd9803006fbf1fa15444d94bd31a679430ef6e353fca693011256f8911`  
		Last Modified: Tue, 02 Jul 2024 07:06:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:61d236518662759dbea3e20daa3f0077b1dce69c7933f0263d037ff1567dcf10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7036129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97271e61cffb033db88848b513ce66a912f792f1edd1183c250a697ab42fba4a`

```dockerfile
```

-	Layers:
	-	`sha256:c0aa2fa529e92a942ab9da631c4a23cc2685f0ed627a8b2d49de2f29d30d4796`  
		Last Modified: Tue, 02 Jul 2024 07:06:57 GMT  
		Size: 7.0 MB (7022278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef338adf73b06ea4883ded6e0c63544e3e6cdebab675d7b3b4d395a99ad9b3b`  
		Last Modified: Tue, 02 Jul 2024 07:06:57 GMT  
		Size: 13.9 KB (13851 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b240a8527b4b7cd2f9370a045d04d935156739ea81c0717bd7a2734708917a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225556764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4361e6e5228f99b3ec106858fc8b9c54e00b772cadb5373278de63f1eb3e6f2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15853bf8cc7cb890eaf09b1c679e02958728ad26cee6a9f618aca04b89974d99`  
		Last Modified: Tue, 02 Jul 2024 09:12:42 GMT  
		Size: 102.7 MB (102700427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded1aedbb29f746f14517c1a96e649cf16564c09ed3e40beace7a196aade626b`  
		Last Modified: Tue, 02 Jul 2024 09:16:40 GMT  
		Size: 69.1 MB (69134038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5b4db452ea8db81fa8e1ee8518363b9e11793bd190c21e105d6010ef0db1bf`  
		Last Modified: Tue, 02 Jul 2024 09:16:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:35ee4209e1ccd6e8d84f61d932b93aa78bb1860b165dc2430b67ac6f733b08a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7042386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7bda2853d87b4652bb0d0102c875c3c2105c7821ecd38c1087d9386baccef3`

```dockerfile
```

-	Layers:
	-	`sha256:8e89fbc92820486615bd99c87a33b9bd657f6acfb42e137a0af8224c7e14d46d`  
		Last Modified: Tue, 02 Jul 2024 09:16:39 GMT  
		Size: 7.0 MB (7028000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4c23739374f3883faf20306e5788992354d2014f1c0f04a7bff80df554e3ed9`  
		Last Modified: Tue, 02 Jul 2024 09:16:38 GMT  
		Size: 14.4 KB (14386 bytes)  
		MIME: application/vnd.in-toto+json
