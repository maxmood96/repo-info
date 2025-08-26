## `clojure:temurin-24-tools-deps-1.12.2.1565-trixie-slim`

```console
$ docker pull clojure@sha256:7f214f0ed013da3441e4f2d476a742f27894b9e9ba5309496d98b2669c936cb2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a98382320e74e999b26e78235b4e7d132a39d2bc05c41002828bb7255b595341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191731874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875fd323993c9d8a075350fc53bf028b38d47c3aa60c65c61f1351375e87df2f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8416f29fca1026c5c7a3c8384a49ce4c6feefccc6be86dab25a49668aefcf36`  
		Last Modified: Tue, 26 Aug 2025 17:28:26 GMT  
		Size: 90.0 MB (89975231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca0b19c0abc80869a51987f99243690c29372c1f15a5ddfe013414c844ac57a`  
		Last Modified: Tue, 26 Aug 2025 17:27:40 GMT  
		Size: 72.0 MB (71982317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17045209dfea8885051d2086f1218a9bcc2b6c2eda6d8a8389b8e3fd899dfad8`  
		Last Modified: Tue, 26 Aug 2025 17:32:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b7fc08c00879e3915edbf78e7d9813b630a58de2bd0e4f6cd96e4535c6fb79`  
		Last Modified: Tue, 26 Aug 2025 17:32:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c5b0cdcd9047e8c2ce6f8227289fb6fa3804091022a6701d020de54de93b9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06fc585ed345baf88b59889eea8852f1c8c91f8a0335d5d292b28b0ec5934f7a`

```dockerfile
```

-	Layers:
	-	`sha256:8ff5293c604f843de81052eaef13853d42df2c0d70adbe1bdb199983d41ec6ef`  
		Last Modified: Tue, 26 Aug 2025 18:43:05 GMT  
		Size: 5.2 MB (5205885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238763448f0a2c268f846f38d663c74e8a5bdbeeece932b34f910110dad7f59c`  
		Last Modified: Tue, 26 Aug 2025 18:43:05 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aafd0b580bbf84593e20f095854e71caa4e0c939d65c4788c500e44f7a2fad91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191033243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c853b4fc46f913fa3c8f5979040089f1dfab9831424a5f769dee3bab8e29c30d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe54333b06ad8dc6a1c19356b2654e06d357097398ccfe7bcc23b46b25aca1b`  
		Last Modified: Mon, 18 Aug 2025 17:25:14 GMT  
		Size: 89.1 MB (89092501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432e489d4777f64036ef55d59490f9cdca26a201ab682742854572244a16b1bc`  
		Last Modified: Tue, 26 Aug 2025 17:59:07 GMT  
		Size: 71.8 MB (71803654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c6f7ab409941e185c29ab3bd060e825a11db4cb6fb8efffefaccc9c5cb6fcf`  
		Last Modified: Tue, 26 Aug 2025 17:58:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e63a0f205a7516d2859b9e9459ed964dda9038a7cda1e233e603dff006e2519`  
		Last Modified: Tue, 26 Aug 2025 17:58:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:18c0a50e45cd73738202c7c7bf6a0113157e5ef7a592da2ae1ad49b977e48552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb24945a92b9347949d8e66d9b7a0bbe70275237a844f3086153d69db8e2035c`

```dockerfile
```

-	Layers:
	-	`sha256:d1df14bd68222f5c79aaf51a403e88e6f324b8a790f53b9f03ebd0b2c2bbb719`  
		Last Modified: Tue, 26 Aug 2025 18:43:12 GMT  
		Size: 5.2 MB (5211651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe98071523545ab8248cf53257d917533ec297ddd1b68499a9af9d0c03a86a24`  
		Last Modified: Tue, 26 Aug 2025 18:43:13 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json
