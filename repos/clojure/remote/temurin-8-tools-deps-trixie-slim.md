## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:c2b912a2246d8acf4b6ff6cbe424a843edc917ebc02430618f84941af0d449b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:16e4683c33f4ec8d61f44b1b7f2bb471b9b92e3ca455d772e18d82e7aa18be0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157026183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a7f2c0ce65c3928b433b2d1dceb704b8b78712bf6604f3a79874b2c9ff0ca4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:56:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:56:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:56:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:56:49 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:56:49 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:57:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:57:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:57:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb26bb10b8a9b22874e72e4f8292d48da30d5415bfb1394c19ef42f18f56ba1c`  
		Last Modified: Tue, 19 May 2026 23:57:23 GMT  
		Size: 55.2 MB (55198698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9fac6b181156ff6732f9bbb9aa44975c3dfa2b49bdde7cce4828920e106dfb`  
		Last Modified: Tue, 19 May 2026 23:57:24 GMT  
		Size: 72.0 MB (72046918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d05d369f813daa677058bc68320b83b85600360c008b0c5b4445f022bc2cbf`  
		Last Modified: Tue, 19 May 2026 23:57:21 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5e7ee0820df379c9cd9b87db4742ba921b81d42ad001901b2a2f3a1e95a4746d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0279a072dd31b9e508252cef8432722406e34e6cb875fdd3e254dac41ade24a6`

```dockerfile
```

-	Layers:
	-	`sha256:751e135b64f41e7c92ffe3c6b3adb3b3fe33b191029670fcd807928ba873fc21`  
		Last Modified: Tue, 19 May 2026 23:57:21 GMT  
		Size: 5.4 MB (5380327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b6650081398d6e0e7e7d48a9755d577c9b36bf990a892f0ba0e6d5f7fbfee0`  
		Last Modified: Tue, 19 May 2026 23:57:21 GMT  
		Size: 14.4 KB (14381 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:63847f5c965818a5854ecf7d124566051240a3fd3eb78f126e3197526277cfd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156287058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2648ed063b4b7a0e41806a17170fbf46623d1487dfb51a3edc9912cf9f32238e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:03:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:03:25 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:03:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:04:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:04:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:04:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa64a52fb10af27921f15bfa4a2f9c8430e12cbb0e781cfa5868fb6ce1dce49e`  
		Last Modified: Wed, 20 May 2026 00:04:00 GMT  
		Size: 54.3 MB (54272922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607e11eac47a663587b032c4fa8d49b205738feb3f31f57f82c245fe2d6d8a3e`  
		Last Modified: Wed, 20 May 2026 00:04:40 GMT  
		Size: 71.9 MB (71871571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5671a17c7a7b205787bd716b926a194ca0bb565ec5ccbdadb19da61cd2273904`  
		Last Modified: Wed, 20 May 2026 00:04:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:57826dc8cc065e606eb0af4f50efaacf20a97989454d1ee804894f6fa29a16b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca344691ad1ba8d1080c67b5b4306438dad8b9c2090972a44c4d957e3c6dc77`

```dockerfile
```

-	Layers:
	-	`sha256:9752964221ad15a5b1fb0f385cdd7ae29d2966e14d03eb72b05efd4889f0ba1b`  
		Last Modified: Wed, 20 May 2026 00:04:39 GMT  
		Size: 5.4 MB (5386788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0867f504c5f69c2dd085795cf91e86f3448001ac36d8b03065fab66c92c6768`  
		Last Modified: Wed, 20 May 2026 00:04:38 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:76b74ae6b98e7594b095ff16fd8bbce014d13364ffed2bc29bb01e08a696a720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163736536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef15ffaf6f21970485991256439ca55268e259ec703e903b2956c2da8a154ef`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:44:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:44:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:44:26 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:44:26 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:47:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 05:47:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 05:47:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c11b5f3a4a015128bca89c0e32301100f65c70ad718542cfa4e67c2e91aa807`  
		Last Modified: Wed, 20 May 2026 05:45:25 GMT  
		Size: 52.7 MB (52669123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a895bce667da81ac48ce48130aedbb76fe84145aa2b9fcc228e86bc11ce91`  
		Last Modified: Wed, 20 May 2026 05:48:09 GMT  
		Size: 77.5 MB (77466316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e81b5117dc760871939241c2aa68ed6f4bbca27ca3e36e71a03119cfdecd585`  
		Last Modified: Wed, 20 May 2026 05:48:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8659b50e64ea942274ae08a8f341b924667daf39b0b17b59bafc495d5e84746f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dddf92f3a19cdb1cf996732d9873d8e08804b1155e3813955856fd566bd6e7a`

```dockerfile
```

-	Layers:
	-	`sha256:b882c269b175a91355915872cde508390f4cc5a048fecc8c197b70042d7c2f63`  
		Last Modified: Wed, 20 May 2026 05:48:07 GMT  
		Size: 5.4 MB (5385293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c78488f8cc36794d260c3fe5f97c0e31eabb3224b684b4bfe157e4aeb17b7a`  
		Last Modified: Wed, 20 May 2026 05:48:07 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json
