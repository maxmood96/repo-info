## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:a579446d35d76eecb3fb8b155a3a8c8081f580f629bcc4010c4e6d24d93c294e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:533192d1fd882272a925a27a91bf95c9305f11bd573c9f152bfc87fede414300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246466914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239dd1f61592a6ca851b7a1610edb5ce60c82f20bd70377c3167c832ca091203`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a789709f2dd5fc1d2372b3620e4f1b0148dcf8e8521e7611478cd79636fdd5a4`  
		Last Modified: Tue, 21 Oct 2025 12:51:25 GMT  
		Size: 144.7 MB (144693294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8d40d302a33fa3d52f93daf9a43713b87bacee4ffc02363fbe0c5223ba63b4`  
		Last Modified: Tue, 21 Oct 2025 02:22:35 GMT  
		Size: 72.0 MB (71994655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcef85c10f1a2d40eb64b439f8085f997f2ccda27f64c9ed24a8ac92b6ebf4c`  
		Last Modified: Tue, 21 Oct 2025 02:22:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e494813e21b99c7670d2a9311d3900ab2d678284dc81f64e5a67c398c3fabc`  
		Last Modified: Tue, 21 Oct 2025 02:22:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b548bd86c0d48200487f8adb8692c1b6a60b898b9f1855ff16669da22da7bb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bb00577dd26ef9122abff669c2a682c011716ec13106a04a48b2302a0f0e0`

```dockerfile
```

-	Layers:
	-	`sha256:010fddcee7c4a641151c6e877b845fbbe1f3169cea894865097a89606da74543`  
		Last Modified: Tue, 21 Oct 2025 09:40:30 GMT  
		Size: 5.3 MB (5256167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7428974dbfcdaac43ee06e43f0a0f82d7637f175312e76bf00548344ae588c1c`  
		Last Modified: Tue, 21 Oct 2025 09:40:31 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20f4a42dada708b24f1c668165295da62837f935703a22a2bdc689b3c1ead9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245493572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d20d2016bc50ecb57259211cda54492af73c291dadd9b2fcc61c24c463f44f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b98c886e64e9b25db06613bc67008841efc163ff091149cdad51d95001052`  
		Last Modified: Wed, 22 Oct 2025 09:05:03 GMT  
		Size: 143.5 MB (143542159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4c2f2e9ab5527bd70ee14cbd8a64db9d3669c5f5bfeaf9ddbd2540795737ab`  
		Last Modified: Tue, 21 Oct 2025 02:28:36 GMT  
		Size: 71.8 MB (71808246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353586e0f54867057fbbb92746af277b5571ffab49df7e3fa9afefb40e75e2d4`  
		Last Modified: Tue, 21 Oct 2025 02:28:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fd30fd14af59e108502379d2734fd4244949b6fd70f18bd089596145efb649`  
		Last Modified: Tue, 21 Oct 2025 02:28:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0bdafd9e127bd4de3c6be967ef44855a863a5215a1a73e638a2dbefd51bbc288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b8d9055366f3961e068ecb65190ac825c2416af682c24c25725f77fd5d82c8`

```dockerfile
```

-	Layers:
	-	`sha256:9b0877977fa62140e1f3b34ca3d411e798c85fc8440f0b823af2774f0d14e166`  
		Last Modified: Tue, 21 Oct 2025 09:40:36 GMT  
		Size: 5.3 MB (5261936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ce4fe6d546eae10304c170f08e13c34fd7c748cd11dfd1dbb5ac4da2fee588`  
		Last Modified: Tue, 21 Oct 2025 09:40:37 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:509be3ad9dad62da786fc2dfd7ebb00b5fb866bb9ac031927e1d6466ffdd635d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255367328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e6f80ac54c4b93c540281a51f8cb3820ac2e7e68b91cd15a57b12e1135dd57`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52385a3e6cfad3a2f80cda82b28f3ad981ef1c6d85b4aed63025a1371df43a50`  
		Last Modified: Tue, 21 Oct 2025 15:52:34 GMT  
		Size: 144.4 MB (144372874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7e6240e7591a5e823f735a974dee2c9b2e1b275879bb4c0ed9e40a0c18723a`  
		Last Modified: Tue, 21 Oct 2025 15:59:50 GMT  
		Size: 77.4 MB (77394893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dae714986f2e82d0fddbfde2fe3e3fee24781880d82c7c8e49c8b1272aa412f`  
		Last Modified: Tue, 21 Oct 2025 15:59:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694e6f1c94a8c8e6a81d86a24c7ed7ca880e11e4b2e6424981ca405a156e27f`  
		Last Modified: Tue, 21 Oct 2025 15:59:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6cfe6e2fd6ec5af6f1f71691cb672dbaa8321ced5b31d49dfca18f5bcbfde1be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d95be2156e3eb35b5c2f7565b01b0c5fb6465f995bfa4c2558296c8af98b29f`

```dockerfile
```

-	Layers:
	-	`sha256:9472881cf85938e075101427904e751639dd6f240bced9903d0b52bd1f786670`  
		Last Modified: Tue, 21 Oct 2025 18:38:17 GMT  
		Size: 5.3 MB (5260538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce3457a7864ed747c484e17a0b89b71bc240636bf75d6723184424766af9a51`  
		Last Modified: Tue, 21 Oct 2025 18:38:18 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:bc4f644f800dd594c14788f623ce9fbc9dee0744601c98c4dbb761f99c86f6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237733146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10df0cdbb2da039cf7dcca82f5aad018dea2b6d5e579b9c12143858e3f7624cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de474e3dd67de6ede0e921395a3668a1af187dcfd0cd62fe28f9cc74e299d6fb`  
		Last Modified: Fri, 24 Oct 2025 01:09:36 GMT  
		Size: 138.6 MB (138575664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16c1db97e0d9c3a35ae3058dc5aa6bf66b6c9a7bf1e92724831f8deaa50add`  
		Last Modified: Fri, 24 Oct 2025 01:49:35 GMT  
		Size: 70.9 MB (70880786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848be88cfa88dc4b9c4bfa622ac56f296571d333d95dd42d0fc49eef2fedc1aa`  
		Last Modified: Fri, 24 Oct 2025 01:49:28 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04eb20d9250c9d4e704356ffc7ac415ffcac5f16fb8638234668d8a6003e64b6`  
		Last Modified: Fri, 24 Oct 2025 01:49:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:206cb76932e2e0636c1fe423609e8dfe34b71482790b6bd7bc201a126bede74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335df4d5027854b74e8837bbc5ca593e0fb2d2b755ea8e8101e7e0f71f56b490`

```dockerfile
```

-	Layers:
	-	`sha256:bd0c0570521ca94e2eacb8cd09cb11359399a4a8f6ccbcba3d5225cd12324e51`  
		Last Modified: Fri, 24 Oct 2025 03:35:50 GMT  
		Size: 5.2 MB (5243712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021adfff7ac7dbae96bf01569b2f0f97694b9dce45052692111454acdcfb1838`  
		Last Modified: Fri, 24 Oct 2025 03:35:51 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7ba50ec0d231efa95e3699a2bb9fe731029be42bf2c6e7210383193fa53ae30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237515564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebcae3bce3f933c703b0623f182596a6831d550193cfdc839acbe9f947cecd6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06700ca270596eaea1831cfd84f4899a01382a5a211281abc3e907b46574ccd`  
		Last Modified: Wed, 22 Oct 2025 21:58:46 GMT  
		Size: 134.7 MB (134723657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dedad781071ffbbf6c718c144688169310d6dc13cd3b5656d07bae0bcc40a33`  
		Last Modified: Tue, 21 Oct 2025 22:23:03 GMT  
		Size: 73.0 MB (72953609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb051d82a503c928b51792f141cbc7534ec6007075f1e91b6b6a47ba3dc3c2e`  
		Last Modified: Tue, 21 Oct 2025 22:22:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbd7305c168cb292def4d2920e63265e6a6587ab9faf1e957a669d3bd5ba177`  
		Last Modified: Tue, 21 Oct 2025 22:22:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8baf432ae627d3041102dd5eb1edcd14ce70291f0d2796221b378666ec72e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91d190d0f65d5a0aa10cd65094a72372e838e5bfc6337154666416106507f9f`

```dockerfile
```

-	Layers:
	-	`sha256:8e60a8da61478362b59d00dfab8e853bac921b3f6d2613cca073047dbf7083a8`  
		Last Modified: Wed, 22 Oct 2025 00:38:06 GMT  
		Size: 5.3 MB (5252091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da4ecd9f8a4470404b127b0ad619a45463efd8da395c8da6c08322bdf52f9f2`  
		Last Modified: Wed, 22 Oct 2025 00:38:07 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
