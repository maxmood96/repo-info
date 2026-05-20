## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:5cb4778850818e95829d9afcd3351353386d988ad14990340ec812b1c7b6c5c9
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

### `clojure:temurin-8-trixie-slim` - unknown; unknown

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

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-trixie-slim` - unknown; unknown

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

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cb436a1711a40d8908cdf5849a94f7f54fc193a33ef3e131dc09ef27c3606099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163724454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e879741a687c80fe2e60c676a788dab7151c7643c7881f8aa2c1511b344f74c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 21:49:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:49:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:49:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:49:10 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 12 May 2026 21:49:11 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:17:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:17:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:17:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6108e5c2a2245ec0c51d22b23687faec2598356811a7675057929aac5f8deda`  
		Last Modified: Tue, 12 May 2026 21:50:14 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909f341bd605d5ae237f974afc0b5e84f1a8365aff56f6a92abb41b8c29f37d1`  
		Last Modified: Fri, 15 May 2026 20:18:26 GMT  
		Size: 77.5 MB (77456569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639a024378aa5857d0709ba9a019824b7f62c0ec88cabc150fc75e19eda047d6`  
		Last Modified: Fri, 15 May 2026 20:18:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4f3d4e93d4ad08e797f9b27e2bceadd5ffb37c08e60903e8ce472d4a66ff9c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0841fbd6ae488fc6a62896e59febbb0876d588776cd841e767223d7686b85395`

```dockerfile
```

-	Layers:
	-	`sha256:7885d99b972e7c9d2295a8236daf89c568df26495d344516184a26bdc9a1a0d3`  
		Last Modified: Fri, 15 May 2026 20:18:24 GMT  
		Size: 5.4 MB (5385179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971484feee30b14fdbb24eebda0d1a1c3762f091b344352f2418a2b232ed6d4e`  
		Last Modified: Fri, 15 May 2026 20:18:23 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json
