## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:fb37e97da9834d111e67dcf3c71220c07b08420f9366b283651af6c316fcfc48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ae4e3c138c85c84bdf4c34adba48cc2e089d84485a78be5ce4fd0a164e743d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156943688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f97dff986e3c86d84c3bd84d2190e1a2c5de12a39a1d107b404d127186ae769`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:52:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:33 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:52:33 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:53:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:53:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:53:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8362d916c99f3bb6ea102c595ddc32c0a7078d13606452e9b735932635b03336`  
		Last Modified: Tue, 24 Feb 2026 19:53:04 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dfe36fe7db5c430b5f01343060839548aa081a40aff5458a2877d0255a9081`  
		Last Modified: Tue, 24 Feb 2026 19:53:45 GMT  
		Size: 72.0 MB (71994353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27833084c3442a859d5e396bf4097d94c34e06205bdd050e83c37906b7d3703d`  
		Last Modified: Tue, 24 Feb 2026 19:53:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8ba5ec559335fa940d168f56b4400c043c906b9328b5685567b78a53b34646d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03991517924139c6ba014af0582592f6b7de1c993a83e2fa67f1eacd0210273f`

```dockerfile
```

-	Layers:
	-	`sha256:3b7bbe12129928a0641838618cdbfae5c322e1f5902cf193c9f15d9ce0321890`  
		Last Modified: Tue, 24 Feb 2026 19:53:43 GMT  
		Size: 5.4 MB (5378538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7231c411135ae657ff6807fdf8aa43978b793c6cfdbb3db8a6d7c7c0b6d38557`  
		Last Modified: Tue, 24 Feb 2026 19:53:43 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3829f4d1a04e256db5111dcb611d40bafded29118a9fdbda36e40c6b30d369c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156200179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64e303c0445bb808a1de1443e58fb2549f64013f0b6cf246e2da78a7e9b2674`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:04:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:10 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:04:10 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:04:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:04:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:04:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1778e3b75b22d1e590ba68beb45a4dedcc1893c547192fc892f6b9778a812f0`  
		Last Modified: Tue, 24 Feb 2026 20:04:47 GMT  
		Size: 54.3 MB (54251627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212d52cf5534a02c86a6d1643022ee371cb0e44648695353a996e097336ffd33`  
		Last Modified: Tue, 24 Feb 2026 20:04:47 GMT  
		Size: 71.8 MB (71807811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8af6e8d7f55dca1e4beb33e7a996218b87e173467bf6c21542cb8f99ca518d`  
		Last Modified: Tue, 24 Feb 2026 20:04:45 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d84599c30d3d3b6e234399ed2b527f0b0ba91aaf7d068100b1480d58d31f0b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7031d103fe5395e647f7dabb3834da2a63dc6f37cdc18c5390ee02b0ca8c8058`

```dockerfile
```

-	Layers:
	-	`sha256:7230459c2ba3a853adfc5a4679dac4d7f1b90bcbfa411b64352e2f793189bfd3`  
		Last Modified: Tue, 24 Feb 2026 20:04:45 GMT  
		Size: 5.4 MB (5385007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5eb65ae258bc982bdbae4257559d33adfdf8a754036b549db964e5f09a0b79`  
		Last Modified: Tue, 24 Feb 2026 20:04:45 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:76a607c63955a1c995f7cb905722a1ab8f0df28824ff9b363c3a06fafacbc703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163641758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2664422fe25744d74aa4c7187c585f55d35bc9cd78de34b3e24b56811fc6c979`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:00:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:00:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:00:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:00:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:00:12 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:07:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:07:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:07:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e89dcc3b95f00f17f7b2d6872744c6220cb1fbbd573cd216d9413691c73b51c`  
		Last Modified: Fri, 06 Feb 2026 00:02:21 GMT  
		Size: 52.7 MB (52650394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccfc408e8ff54ba791a45ce0440d8c1e26e720d22e4eaf8ee74a5fb7f0f675f`  
		Last Modified: Fri, 06 Feb 2026 00:08:51 GMT  
		Size: 77.4 MB (77390534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26c858ae7504b91d032e21c47b2803e68ab2e6aacb9b231c2363351a693b12c`  
		Last Modified: Fri, 06 Feb 2026 00:08:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a6e8dabec270328dbd534889f63614e6b202bc5daa2410cddc922ca01dc9fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2fd1d70e2f08056196d73599c77aa86c11e01b6ba524456255e9ec858a79e7`

```dockerfile
```

-	Layers:
	-	`sha256:07f2c7a5a993eb6fa0f4acaae58ced41e46e53c051d6deee327d5839c5fb0079`  
		Last Modified: Tue, 17 Feb 2026 23:32:40 GMT  
		Size: 5.4 MB (5383504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:722b385c8bea3be1a0285e6772d019ff7af30160a3ae3ec64a2f952a587c2685`  
		Last Modified: Tue, 17 Feb 2026 23:32:39 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
