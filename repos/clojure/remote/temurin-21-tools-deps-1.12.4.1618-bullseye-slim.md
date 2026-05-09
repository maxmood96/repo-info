## `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:969b3f1f25f0e7a20563c2d33b9c3747ec435ea40714f927cd0b05057716771b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b088dc9398b090a2379b0596bb4547454b47bf866bba5e89fc97124107a124a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247612202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2422b122a502c484a17dcc1893333b79768f3fd22519e95ba9b5968b0d460d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:18:20 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:18:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:18:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:18:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:18:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cb0957507bf8a88ebb1681e6f07667f49f946260e5789834ba806c0f33af96`  
		Last Modified: Fri, 08 May 2026 20:18:58 GMT  
		Size: 158.2 MB (158166903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f16dcd77e14567b039309e333d9a3d8912f6b2e63b62ee660e7aefe1b920dc`  
		Last Modified: Fri, 08 May 2026 20:18:56 GMT  
		Size: 59.2 MB (59186299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13baac88fdd28534dbd81289e023bd6b6201bbf5d5c5f1fef67cfcfa4400f34`  
		Last Modified: Fri, 08 May 2026 20:18:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a611e1ed374015a4acc9a5870d1d369372f7898493ed0f9693cc545318e3b8f`  
		Last Modified: Fri, 08 May 2026 20:18:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:54b33ed168e3e8c7d1bb46517862fdea2bf9539d5bc819c8ebb2e278ca92eb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb4cae1bf1edb75fa5fd4b84367f1732315775cd4240ac89e7c194f73633583`

```dockerfile
```

-	Layers:
	-	`sha256:ba63efbf01e7ca93b3eaa4a6f8a1831455328c5c802ab509f099b6d713f64d40`  
		Last Modified: Fri, 08 May 2026 20:18:53 GMT  
		Size: 5.3 MB (5322532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a29c4530d34772cb42c57bb5d2148a44e438baec762ba671c36693972a8560`  
		Last Modified: Fri, 08 May 2026 20:18:52 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e26465d08cae43d0fc3a3cf8d77ed32f0649e5c236921a00030858c23e7d83e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244536018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665a17dfb734655930edd7811432cf5a4f1c8c41ca4041b72814109cd794f27f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:23:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:23:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:23:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:23:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:23:03 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:23:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:23:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:23:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:23:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:23:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9df05463dae6a074b2e91e199b5c2b504b37b6db0947513a9bae28403bf954`  
		Last Modified: Fri, 08 May 2026 20:23:41 GMT  
		Size: 156.5 MB (156461190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ca440034f4e5b5b53c7833b930fb2036c3726f3562184dfa1981eb57a5d10`  
		Last Modified: Fri, 08 May 2026 20:23:39 GMT  
		Size: 59.3 MB (59331196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da218575ace194f96bfe302d36c5fadca990dda2ee4aa494959d6a54dd419cf3`  
		Last Modified: Fri, 08 May 2026 20:23:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb9c0076909ccb7a5795f4e2e94f7f124c01c68463030c114502f977d53e804`  
		Last Modified: Fri, 08 May 2026 20:23:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8750a93fe46f9cd3bbdc8c2920fec931348876dad33124f139408f029f79d4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5344372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb94a30477036cda1fbde8b3300040242899263f437b656cc41f62e8508739f`

```dockerfile
```

-	Layers:
	-	`sha256:a37f295c45f12d2d9dbba7c2b80ccf4913543f0fcbd8d94fcfd587734e4412e6`  
		Last Modified: Fri, 08 May 2026 20:23:37 GMT  
		Size: 5.3 MB (5328264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcc28d399c24c79ea513f4f54c97e28e8209db5e1c82d077f2f0d5265ae9848b`  
		Last Modified: Fri, 08 May 2026 20:23:36 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
