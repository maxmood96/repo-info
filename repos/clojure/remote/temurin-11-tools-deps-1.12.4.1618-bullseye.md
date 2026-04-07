## `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye`

```console
$ docker pull clojure@sha256:c24ed36b8f0ddd69138cd65834fcf254e5a83a9f184e2e13ad7a2dd74af5e604
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8f099dec396482cc3a7e467a262dac76402c18b0ef44afcf8e79dc26afbcb44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269158069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934b860add2a8981fce2bdb9a3ee6502da0b0e23393ef53ddf5c40a1022b2ec4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:13:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:13:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:13:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:13:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:13:53 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:14:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:14:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:14:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389573fd979a2e780bcb771bd3db65d0cf5d14202df631562f9586f39e3d98ae`  
		Last Modified: Tue, 07 Apr 2026 03:14:31 GMT  
		Size: 145.8 MB (145806887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cfca6af5be9bcb89d61ffbd3447eeb7df11618a4f3121457086575340a1570`  
		Last Modified: Tue, 07 Apr 2026 03:14:30 GMT  
		Size: 69.6 MB (69587745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbccb668a22b9f85a3b6cb3c892fb13aeb0f0dee6890ea75d058857e6cc31f5`  
		Last Modified: Tue, 07 Apr 2026 03:14:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4a8168d6ce502ec4bf2fc23cf5f0921654398b2619c6b9fbfc39e36abc8f4cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62f1ccc0d4379ffb60052167c0bf23fb79b03ef171e2fd1b3f2e1acd80adf66`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f17540f4eea645bf3b11d8315732d1e514bcda3eec4d28067a80251f71479`  
		Last Modified: Tue, 07 Apr 2026 03:14:27 GMT  
		Size: 7.4 MB (7427794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5ce32217275b25409584317665bb8ec8c208911b86b82379bc68ce823666bdb`  
		Last Modified: Tue, 07 Apr 2026 03:14:26 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d35b86f57b9f3ea1df134200bf97671d476cfd8c15e82a555f16fea0a4d5f44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264476704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a3c7f6270be57caf924b2a5b5dd29d1177ada855d35f3990d843cbc1fa8f76`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:24:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:24:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:24:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:24:38 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:24:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:24:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:24:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eb42e9709d585c47c6f28913f6b182ef22e20152eb224c9d21f4aae5df132e`  
		Last Modified: Tue, 07 Apr 2026 03:25:17 GMT  
		Size: 142.5 MB (142500071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70ba1d410d4cd4709272f9917b318ab85fba2f4d210ab685e22954054fc8b8a`  
		Last Modified: Tue, 07 Apr 2026 03:25:16 GMT  
		Size: 69.7 MB (69728374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff35f14b7725da5fdc6a43c9e00e274617cdb71b46edbf9a363169be71d7e48`  
		Last Modified: Tue, 07 Apr 2026 03:25:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:acde3902caa4e9b265dc0ee70abbdf1fcc8a86845ef04842f978a8f064000371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7447837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ecebe6ebb2213685736393854c0c7824f30faecf52c0e72210d633c837d4020`

```dockerfile
```

-	Layers:
	-	`sha256:0483ab106e294cf10c18412fa1f8fe07f519b0bbc0384b53e4e7deab9383475f`  
		Last Modified: Tue, 07 Apr 2026 03:25:14 GMT  
		Size: 7.4 MB (7433511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d8fe119b8dffa21fa045fc5ebad82e254f62a6c00aa7f380f951c804b21286`  
		Last Modified: Tue, 07 Apr 2026 03:25:13 GMT  
		Size: 14.3 KB (14326 bytes)  
		MIME: application/vnd.in-toto+json
