## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:59f72b233f2f9887997aa8fb627f35ce78ec0167600ad73e6e5dd15d8073f9cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c3c59acc7bf5ef753baab4de20deca29f721297088df3d8f2b976030543fd95e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278453847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24838e0e3742315b9b0865f7f4064f051c8d505078c9713a51f0a1de6d1af3c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:19:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:19:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:19:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:19:50 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:19:50 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:20:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:20:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:20:03 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:20:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31f04f1ebfe53326277e89e1df40a80077125bc798abf9e43199c7ed8e0531f`  
		Last Modified: Wed, 24 Jun 2026 02:20:30 GMT  
		Size: 158.2 MB (158166945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84617bec37017846869a68688ac4d5ebed114eaa3ef184d4a160fd8b56bcb2a1`  
		Last Modified: Wed, 24 Jun 2026 02:20:28 GMT  
		Size: 66.5 MB (66512850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ca128dcee5234506aa76baa4e292c258a7cfbb3a936fe842031411b27fd322`  
		Last Modified: Wed, 24 Jun 2026 02:20:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765ab025fd1af8c9997205655b9756bf7b028b4c6601911ea6126c9e157d6d1d`  
		Last Modified: Wed, 24 Jun 2026 02:20:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:18d49c39b8c215e436a542d4a3547d2fc8930a1472b8218990fd19ff13ecd2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5a51f634dd94734414a7505d235767adb509d53419d20b3439d68127185442`

```dockerfile
```

-	Layers:
	-	`sha256:160f7cb009637bf75373438d39cb816fabe063277ef9851b37ca51d4aa199cc1`  
		Last Modified: Wed, 24 Jun 2026 02:20:25 GMT  
		Size: 7.4 MB (7407301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb602fb66dbfe251209804231af875666b88c2d8bbc2b015a8bc8e7794963e7`  
		Last Modified: Wed, 24 Jun 2026 02:20:25 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b73ef91c6b3733efd4f5499909340d5374eef18381e22f1de40f002c70d749d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275397344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97924d3ea9096b8f941682ee382f57cd8cea82359a54f5672fc02b1ea5a9751b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:26:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:26:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:26:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:26:14 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:26:14 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:26:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:26:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:26:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:26:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:26:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea06dda2bb08149e1087bba2e0738435ac9eab4e409924652481ebf5568e5c6`  
		Last Modified: Wed, 24 Jun 2026 02:26:55 GMT  
		Size: 156.5 MB (156461286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d3f470882f0da7b5932a67f4212d56bf93deba4736a84f71e745fae8152433`  
		Last Modified: Wed, 24 Jun 2026 02:26:54 GMT  
		Size: 66.7 MB (66677797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045c9895dbbff25d22734d77e612ebc8f48cd0bbda10a28ac7571f47b31a24b3`  
		Last Modified: Wed, 24 Jun 2026 02:26:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de0ceca1a3905fe196ad9b9ba7532c2422a3fd891e82b68443cebe395f023a6`  
		Last Modified: Wed, 24 Jun 2026 02:26:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7f1de7a74dccc00da1373e5ec925836c919aa101b2b3cbced6f5388ea87d5a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9de129a15adb4b7b6c5f4069ca665e4ff09b0bf21e9c9f9d69619778c3d83ae`

```dockerfile
```

-	Layers:
	-	`sha256:e978fd6195fc3ec7a08a1b4da895955f87fd3623aa8983e52ee95b5215f923dc`  
		Last Modified: Wed, 24 Jun 2026 02:26:51 GMT  
		Size: 7.4 MB (7412400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e238938b7e2fb54f871fb4474801b8b40d837ec08710bb047258f847f5705cf9`  
		Last Modified: Wed, 24 Jun 2026 02:26:50 GMT  
		Size: 16.0 KB (16049 bytes)  
		MIME: application/vnd.in-toto+json
