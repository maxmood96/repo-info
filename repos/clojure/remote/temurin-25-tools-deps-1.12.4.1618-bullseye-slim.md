## `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:77ba1e0ffbec43e022f218efd1c4de92d12fdf4885fa15fcd2ce8c17aa57c5b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dfbd724f6d4c48b298ee17b714d3bc5cd4fb718abc0af62743def94b08a30087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181698804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721067560fb1267aa6fc6067220d376682f36f0490a6339a3c2439119b97eb2c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:17:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:17:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:17:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:17:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:17:12 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:17:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:17:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:17:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:17:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:17:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5410d930d4456ae13af316713e237da39ab63bd37407f3f315336bd80c6e1dd8`  
		Last Modified: Tue, 07 Apr 2026 03:17:47 GMT  
		Size: 92.3 MB (92256301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c32622ea3b7d113774195cac1cf4776cb010bf3719c0544954e40c87802d807`  
		Last Modified: Tue, 07 Apr 2026 03:17:47 GMT  
		Size: 59.2 MB (59183443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3462b8d18e6536b89855767f3ade2925398e44e448f9b9c231241a098bef1b3`  
		Last Modified: Tue, 07 Apr 2026 03:17:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be33eee5e06c0e2a939e6949f02bd57a5029db674c7079393e5654d62485fb7b`  
		Last Modified: Tue, 07 Apr 2026 03:17:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b56a70eefd473c2c14275046a746cf6a9b46e513119b85d186bb01397293ea20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4700c464bb8d783f836dbfc8d336dbff51f06473d90735df11d354cbdd42e283`

```dockerfile
```

-	Layers:
	-	`sha256:6640a92f28d88811e096c4d5dbe978b88267c8956e2c254b6046736957bbe9f4`  
		Last Modified: Tue, 07 Apr 2026 03:17:45 GMT  
		Size: 5.3 MB (5288147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304c20a6c4bd72be0874ef12db25fcf461612cc76b31c1da7e1fe5008d44816a`  
		Last Modified: Tue, 07 Apr 2026 03:17:44 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b22e02ad1b3d97efb689e397df62f5929031b6d2df01cf51ca468fe1590ae910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179357557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c8f860710d78c6db51ac44cfce423c3c61d7014088a162d596bf0f940698a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:28:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:28:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:28:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:28:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:28:12 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:28:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:28:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:28:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:28:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:28:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd10ca04405aac514ccb623c6854da10f5d6844ba8d74e372d0ba9904a4781a8`  
		Last Modified: Tue, 07 Apr 2026 03:28:47 GMT  
		Size: 91.3 MB (91288288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1f89e96b905295c47a2c9f1113af5fad01d5090f309267420cd84e478c955a`  
		Last Modified: Tue, 07 Apr 2026 03:28:46 GMT  
		Size: 59.3 MB (59323543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da0fbc048549bca2a431219f731354bb9853a45426e21a18c4a381b430f7faa`  
		Last Modified: Tue, 07 Apr 2026 03:28:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf53a79f0c93a770b967de1ec8fd5500e9dba6fe5db9284e6e3911e44ed2fbf3`  
		Last Modified: Tue, 07 Apr 2026 03:28:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a7e597906a683fbeb0b65dcbe0af635528f0d964bad63976de739de39aab8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5310567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a025bb83aeae9a219df23432c4e4e6959ccb39165b4abbbe207299854b8fdd3a`

```dockerfile
```

-	Layers:
	-	`sha256:6fa038306a78f4c808d26f1161bcf16dfb39c6cd39e62bab130c076a41a39f93`  
		Last Modified: Tue, 07 Apr 2026 03:28:44 GMT  
		Size: 5.3 MB (5293900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d920c4a06d7f2deb5fcadc11b26dba3a1a8a3dedcbd319f3e761edfb9a3f1673`  
		Last Modified: Tue, 07 Apr 2026 03:28:43 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
