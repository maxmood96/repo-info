## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:170a9d9ec07adc9c7d611435aaca5784c91d4a473ff5d567b07eeac91561554d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4fe59b2c557c17cbdc6f5cdadddf5d54c35ae3c65ab46f9feaeccad4b2362a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269267425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e806f4676a1414b7dc1acc89f120ab0619bb8447d8af044d9bd09dae439fbea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:17:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:17:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:17:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:17:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:17:29 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:17:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:17:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:17:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:17:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac1e5be7273d6b722c905e2a65e2ace602f8038be40c8073334ea51baa7c161`  
		Last Modified: Fri, 08 May 2026 20:18:04 GMT  
		Size: 145.9 MB (145905487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad82309db2119160659e2d5d14b42b995b4997c1703a19cf4ba536caa7f28c86`  
		Last Modified: Fri, 08 May 2026 20:18:03 GMT  
		Size: 69.6 MB (69597554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21739f5059e00eb74a092fdbc1e3c6ea9c87b4a61c4876753897f56131b93e8f`  
		Last Modified: Fri, 08 May 2026 20:18:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167ebb96c279a7635e9a94f8b04d760e691385b74c0bffce8d1e17986be4a99f`  
		Last Modified: Fri, 08 May 2026 20:18:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:251e3dc0fde7927cc00dd05671cc2ed02e1265baf8d1a7a73f7836137dba2d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7424212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b040832263ad1cf433761662d39e14ff1794a7d3ddd1dc129f671a5892a9b8`

```dockerfile
```

-	Layers:
	-	`sha256:cb52969bbeed86dc46705510e79b26c55c95fd6f471bbd455244dbd2847f31d3`  
		Last Modified: Fri, 08 May 2026 20:18:00 GMT  
		Size: 7.4 MB (7408280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9050afeda8c2706861390f8f0dea24f575ac822afb32644396b09338540e85da`  
		Last Modified: Fri, 08 May 2026 20:17:59 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f290ca4c628988f2a8eee4ea9e9dbf36fe2170cb3f7985574657d6b199a781f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266717204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eda90a862dbf512fdddf648e98a7a70705fd63656aa994d95a0eedcb4a5e5c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:21:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:21:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:21:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:21:47 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:21:47 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:22:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:22:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:22:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:22:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:22:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140a29c0fa5a2db1a0a93ce1b29388c7fc390e1ca731b558c9443f742d2caca9`  
		Last Modified: Fri, 08 May 2026 20:22:26 GMT  
		Size: 144.7 MB (144724336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dc2b242fff7f1c6ec3adf205a47665f9626e013fe6c3ed72e2cebf8121cbba`  
		Last Modified: Fri, 08 May 2026 20:22:24 GMT  
		Size: 69.7 MB (69738618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4b3cd1a3fec17e6e31bd4d028d2bc645e2b506d7f09174e7b8c0805dafd3ec`  
		Last Modified: Fri, 08 May 2026 20:22:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e5d80dcaac7f3d2f0325da323b3da75f2ed5237fe63cb5228e14f69e6d8547`  
		Last Modified: Fri, 08 May 2026 20:22:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5c46ddb0d43702eac48e42d996f69f7c62d370ac509693422b0435afaccfbbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7429429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19720d723e36c6f13c0fb11720024c1c6f65b2e137b69b9e2ebac2bd3e4681d`

```dockerfile
```

-	Layers:
	-	`sha256:3469e142fdcea8bb7048c5e07704a871b93ec842160f7a57e3c4db7bce8bf21a`  
		Last Modified: Fri, 08 May 2026 20:22:22 GMT  
		Size: 7.4 MB (7413379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dc1a0cf4a9affdbe4f94ee3db750b87c093ff361d55b498fd47971d034170fc`  
		Last Modified: Fri, 08 May 2026 20:22:21 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
