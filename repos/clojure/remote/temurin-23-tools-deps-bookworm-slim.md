## `clojure:temurin-23-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:bfe6c6ee647ddbbe53ad7b6a2f21fdc2476d125b09987399377259ee49ad1968
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2137aab221f9d12cd15e765648b321977f98683e2dc6fc15bbcf55849a65ea73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263034898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f36d1ed6541fa0a6c3692203a5900adf6a9aafa5f48f0331bd3ff288674b7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed98ba691ffda5a147463a95b50bb960ccbb68ef7e530d6d1bbabe8f4da5683`  
		Last Modified: Wed, 22 Jan 2025 19:42:44 GMT  
		Size: 165.3 MB (165295134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9283f0d4f5b057daccad099448c45b453d9fa777e0b840b382a128a14f4abc`  
		Last Modified: Wed, 22 Jan 2025 19:42:43 GMT  
		Size: 69.5 MB (69526307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83030996895faf8f89e0db88ec4b6acd106b6b80d52d302df67275eb1915d6e3`  
		Last Modified: Wed, 22 Jan 2025 19:42:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8510d86b6183980bcade406ebe3e136e12ae06c5ada2f91d625594538976004c`  
		Last Modified: Wed, 22 Jan 2025 19:42:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:36ded60c63ab4dd8c68452307b6318747ecb1cd87ff2b0cfa7766ca75b979fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db809610573f6e72eef06b41727e42499a9ddbe67fc65686a6ab50ee6e6414ea`

```dockerfile
```

-	Layers:
	-	`sha256:c01f032fa163ae8daa45041ee4d55e172797ae773d6e8ab52ba333b22920d360`  
		Last Modified: Wed, 22 Jan 2025 19:42:40 GMT  
		Size: 4.9 MB (4917574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e5a9bda9c35d217e99faf750fef84d50b384a2a4aae3d79d2018da03850bde7`  
		Last Modified: Wed, 22 Jan 2025 19:42:40 GMT  
		Size: 15.9 KB (15877 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f8ebcea73c5523fd53fad47fb1d5b644a6b24e17e2ec5442cb37bd54d76fe28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260698168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9039992741acc844e3844b76aab65c68db3ba41f671a10c16519fce9489337e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e6607154e720c7b87f02949a8b89a82092770b07a013f7e734631efff3ec35`  
		Last Modified: Thu, 23 Jan 2025 03:54:52 GMT  
		Size: 163.3 MB (163281815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ccbd719c97db5d2d2c35a707b894ee15c321bf95d1dabf4de4d40acb25e246`  
		Last Modified: Thu, 23 Jan 2025 03:59:10 GMT  
		Size: 69.4 MB (69374280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d6f8781c68e5a24c2d053c75a069e67f2c995b94c91b87ad0ac51cd21da87f`  
		Last Modified: Thu, 23 Jan 2025 03:59:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e25c669c1c2b63b5fe4a1f707d31f8c945fb4dd2fa6e5a947df2b84b841067c`  
		Last Modified: Thu, 23 Jan 2025 03:59:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:16de66f040fb461ab6527686ce29f74e2d46b212350b3d63b018afc85fe23b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28c9621dbd700aaa180547760c3e6c0ec210c416c5f9149108477747ee90490`

```dockerfile
```

-	Layers:
	-	`sha256:8c10964d47c2f0bd0eada6f538d0ed600e270ffb016115ae7f838dbc2742e4a2`  
		Last Modified: Thu, 23 Jan 2025 03:59:08 GMT  
		Size: 4.9 MB (4922714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de0b151a08f3c25da3243f8331afcd33a53fb2f81b786a6f6b04e5dedcdd626`  
		Last Modified: Thu, 23 Jan 2025 03:59:07 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
