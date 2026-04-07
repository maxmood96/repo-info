## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:7b917c074471fd7ed73af0b91954a65105d963c2ebaa756de6571c23a72d0c1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fdaea862711c8728e5df65cf7073c242664e42a771fd63a4e29c887ff767a2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144612065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd5b902c6b7443f96e6e8c3dc69350e78445f3564a381be5657dba62a345505`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:12:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:12:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:12:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:12:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:12:57 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:13:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:13:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:13:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bb7a060f8de16aa54aea5a5d8d6b16069b9a211553d5583add434dcbf53253`  
		Last Modified: Tue, 07 Apr 2026 03:13:29 GMT  
		Size: 55.2 MB (55170110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161ade43d45dde78217fe0131c8686ab03537b67c99e7a250ecf40426954f111`  
		Last Modified: Tue, 07 Apr 2026 03:13:29 GMT  
		Size: 59.2 MB (59183291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f1a09e6f1fa969d8472bc1cb1125d45c4b041fade398d04af3ae85cf5eb0e`  
		Last Modified: Tue, 07 Apr 2026 03:13:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6d758eeae0df431355530560d573ab2b074c7c924156760688ea3854fc7f83de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98961ac0e3666cad8423fc08c1e335fc6f75de1f0a6a361d04fbacfe377f81a1`

```dockerfile
```

-	Layers:
	-	`sha256:223736257d4ec9b4f49101471b16816f5adbb1a64c55a0857ab6f19f4683cf7b`  
		Last Modified: Tue, 07 Apr 2026 03:13:27 GMT  
		Size: 5.4 MB (5441040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:431d166a8e82fb05ee7b68299c28a6d632ce660bc5bc5881d4d4de44450f324a`  
		Last Modified: Tue, 07 Apr 2026 03:13:27 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:88a9eb1d6aae30f7073beab3ae017d053d0f723edd56732806225619a7a9546b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142320421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc3a15c009576555f00b7d2763604c2f652cdca99233f35953c47852671bf49`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:23:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:23:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:23:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:23:27 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:23:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:23:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23af59e170e58ef0a0f701463ecbb7331db8433387f2f9a375762213b0644b`  
		Last Modified: Tue, 07 Apr 2026 03:23:58 GMT  
		Size: 54.3 MB (54251630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839fd890fce15e09c9a3803893ff008ceeeac2b3d610b1bf1f72b89cbd9aba1e`  
		Last Modified: Tue, 07 Apr 2026 03:23:58 GMT  
		Size: 59.3 MB (59323458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d679a5b539fe3fcade3624491f0fba20d1c27177457922345e2c466d340284`  
		Last Modified: Tue, 07 Apr 2026 03:23:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01262ba9713164aa83192c1eb10107cbc64b3c678dc57372139722632a2bf574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e369448a8e15fa8fdf4533650d871a436816deef5d499614797761100c1e90bd`

```dockerfile
```

-	Layers:
	-	`sha256:3ecc8e21550f1429bd083181ec2f5b9caa613672e1acf4ac07f637da80de9495`  
		Last Modified: Tue, 07 Apr 2026 03:23:56 GMT  
		Size: 5.4 MB (5447472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64725a2342196bbbbb7d867b6b142548b694aa95901114cbc91292e7df0cf3ad`  
		Last Modified: Tue, 07 Apr 2026 03:23:56 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
