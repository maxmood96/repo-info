## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:9136a415bbcdd8a31af8658147687cb81110260f4e85baec037f39c46983a3ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3be881126fb4996aa0c9606eacb06d8a95cf52a1825e16a765ff4945cd18c37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234920615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede0442f1517ed74735a6272dd80a605d05b3c004a9c0371cb008c9430abacda`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
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
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af3159ec9bbd5bc101bde133fcb193414f553d1dce0d7fce48ec478ed21ade4`  
		Last Modified: Wed, 13 Aug 2025 16:34:24 GMT  
		Size: 145.7 MB (145658203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aecda5d62c34d0f5537fc9482d1fc4928fba84aa688fb34417a3a140092beb0`  
		Last Modified: Tue, 12 Aug 2025 21:36:02 GMT  
		Size: 59.0 MB (59005651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3dff5b9b25825b927dcdabd028b21a07099078c14444e5e408684c14372c7e`  
		Last Modified: Tue, 12 Aug 2025 21:35:58 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5f3cc672da39e25c2b22a5e4af2222c076a5fdfeb7d7074aec6bdbefe0f3e337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a9655351ca4ac0a42dacd7b81a30ea3fed898d5e63b6c58bba0bdbc8495ff5`

```dockerfile
```

-	Layers:
	-	`sha256:cd9b110c79e3b04e34703cc088c0bf5d379cb8929a0d877df64e8542cfe32cad`  
		Last Modified: Wed, 13 Aug 2025 00:35:23 GMT  
		Size: 5.3 MB (5328179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75134a31030432779d0eb9541556454590d4907b463b60db8cb4814bcd45af39`  
		Last Modified: Wed, 13 Aug 2025 00:35:24 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08608e027b2136a289401a6dbed968f9db8e1211ac66d878aeaf47137c5acd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230349391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ad40b819b10264bdb531fb959b69c3da484db15f4e053d21fedfec37718c16`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
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
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7cdb8bd94a5334c06e7b00196c0e2bd7831f1c9978200756689fa9d8f37640`  
		Last Modified: Wed, 13 Aug 2025 08:46:29 GMT  
		Size: 142.5 MB (142460553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ee386806fc7bcaac8aeacc62af24a5432fc3be38eb9382fbd5c2062472d1e5`  
		Last Modified: Wed, 13 Aug 2025 14:18:55 GMT  
		Size: 59.1 MB (59137701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac579493a959585708e094c7706f1836a844953de38330177a2104adb3c5a5a`  
		Last Modified: Wed, 13 Aug 2025 18:30:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:145f90be8e4e48ddc5ec8dc91601a925483ec0b734008b6b3348a11102e7a776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d187421150b00e488915e953b2ff2312eef2ce71a4ff03d4965e321a97f237a`

```dockerfile
```

-	Layers:
	-	`sha256:6ba57811d06f57f70ed8a8a32c859c8e983fc12e94bb6e52d3a19ce984d60f94`  
		Last Modified: Wed, 13 Aug 2025 15:35:29 GMT  
		Size: 5.3 MB (5334529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0729d7868ead4098f8d272e4e530a1ab942a11972be62cb58dfe8427941c335`  
		Last Modified: Wed, 13 Aug 2025 15:35:30 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json
