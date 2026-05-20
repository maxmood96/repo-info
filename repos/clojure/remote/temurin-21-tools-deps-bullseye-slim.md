## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:25158184236086445fdc4d74e716b1ecd2e11e50fe32671f3c11088d4756ce7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e5e91dd42c78fdea231a06e0165eb0e89fd242a9127f2d318c298006722cda6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247616269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99be6d140276edc5ca7b967e54b82ca2a0e527051fd3547f19e715e931847abd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:25:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:25:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:25:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:25:36 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:59:56 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:00:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:00:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:00:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:00:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:00:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef5477ca1637f8a8b068279a912c5d85804f579aa0a6527b0ab897851dd6bb0`  
		Last Modified: Tue, 19 May 2026 23:26:24 GMT  
		Size: 158.2 MB (158166940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e798250c5d3bb9ced7076b64a90d66db1f4d548cf887713e31934570b07ea03`  
		Last Modified: Wed, 20 May 2026 00:00:26 GMT  
		Size: 59.2 MB (59190688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eae370f024f8b8759db940c6aace382bce59cb7166823011c2f4cd3e485bed3`  
		Last Modified: Wed, 20 May 2026 00:00:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e9ca18683d8d319fac39dfea58c22a6c6bae05d5c61dfb98358328a75bb1b0`  
		Last Modified: Wed, 20 May 2026 00:00:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a6cb19255bd52b506343415110613184ca50aa7f5e5fc02c64ec84b802492153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e775ebfab0a81dd16a558dcc77f426aa6b572cf4b7cf7ec15c9b6379e3a8a88`

```dockerfile
```

-	Layers:
	-	`sha256:40fa04d78e571bfb31c147f3723d6de57e84ed4930cf6b3730f00f2e2a61e569`  
		Last Modified: Wed, 20 May 2026 00:00:24 GMT  
		Size: 5.3 MB (5322530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7355843d593750d0bcb5a508ab405ca3ece9fdfd1b23bd32e9e3234f477987dd`  
		Last Modified: Wed, 20 May 2026 00:00:25 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e86abdcecbcc5427de95ed06033cd5f0bd125f1537cd3b61257069ed20f7a48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244565200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39abcac9ec44cd3acb8c9177004c8a04ba2bed0c449734352c633a8cce9b4910`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:07:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:07:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:07:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:05 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:07:05 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:07:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:07:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:07:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:07:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:07:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe0d4ef32a7aed193c33d6a1a00861490693db6a0371fe6c2f13d746c0e436c`  
		Last Modified: Wed, 20 May 2026 00:07:42 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df7d39cde0e84393176b330cec3bd8135daa8f2fe937978feb71de02587da9a`  
		Last Modified: Wed, 20 May 2026 00:07:39 GMT  
		Size: 59.4 MB (59359864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e44c2f8bc4ef5ea45cbea1786a16168ab50aea8a885e7aa2d360d179375cfc`  
		Last Modified: Wed, 20 May 2026 00:07:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46830c9072f12cd8591cc0233015f550a18bd933284939d357e1507032726cc9`  
		Last Modified: Wed, 20 May 2026 00:07:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bafa421afb2c1b20e786da2c02393984262dd10475d2e0b3649bd659c2d70976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5344370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d9109d93ba2f72eb9bc2f79f3db16178f05c8781b6510299a96345f0d6b1c6`

```dockerfile
```

-	Layers:
	-	`sha256:1eef204d239c9f868bc74f7cd52ff6bcbf697d91cabc4122be5f31994aa09259`  
		Last Modified: Wed, 20 May 2026 00:07:37 GMT  
		Size: 5.3 MB (5328262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cfbd7e226b336b21862386f70db24579663055449d363fba2c0dcf8ea7aedd1`  
		Last Modified: Wed, 20 May 2026 00:07:37 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
