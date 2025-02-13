## `clojure:temurin-23-bullseye`

```console
$ docker pull clojure@sha256:f79e0d2fc4667507359a82a7646203b6bfca3bfd4bebe227c41a4e487a1d511a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3851b77f0686e72c6e805bf67136469b5736ac9f9cd4a78d3cdc30247573904d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288247058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf26750d0c1a730a5c2aad4c7601dfbd254b8cd5680bbfe3342c0f5857b260c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 04:23:03 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5677422e15f022261e12225e1b7497c6f0c894f6a02923084d2b10421534842`  
		Last Modified: Tue, 04 Feb 2025 08:27:37 GMT  
		Size: 165.3 MB (165316181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5008d1f8584d08b12b67045e12bafb243c9e860e115d8b294aeb068507a481e8`  
		Last Modified: Tue, 04 Feb 2025 20:26:47 GMT  
		Size: 69.2 MB (69190964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33e05b5caeb2311b6df6ece7e6c00b2a09a177e3aa2b13997785d178932fb9`  
		Last Modified: Tue, 04 Feb 2025 20:26:45 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0641d7ea35f9e818684ff8a27e35313b664615de5b7b364ba6ba86147438a0bd`  
		Last Modified: Tue, 04 Feb 2025 20:26:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f9bd5cd5eeecc555a6b9bebf13eec9708f299c458c88a6ea974e45518123216d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4148b221341290c889704dfce9bebf04fa68ec3af2db60ae497a5c6d4b612afc`

```dockerfile
```

-	Layers:
	-	`sha256:adb31484f6e7fd0d1159784b67c14f45b9ecca12ca4eda4637beb4bafe5d4f18`  
		Last Modified: Tue, 04 Feb 2025 05:21:38 GMT  
		Size: 7.2 MB (7209560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638cb5c5b39aa09e6ed44accefcc9bc855a8fd9780aeec25fe0232e6c18e3862`  
		Last Modified: Tue, 04 Feb 2025 05:21:38 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6449df1695bd7c8c1610629732f1df51cf2b96b641cb4f94f5c774b7a4a1e819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284899363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291740c0287416dcec2e6c150a60545ea53238ebb643c3c6e7da0d8b05ac370c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 04:34:59 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd20da7c7dc2925173ad8f68cde57ff31d8100b23263e02413cfacd43e2050b`  
		Last Modified: Fri, 07 Feb 2025 06:54:27 GMT  
		Size: 163.3 MB (163341455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361266cbcf0f608b1247bdef65eeb28e45e10b2bd3b75a7eb4dd9985f76dddc5`  
		Last Modified: Fri, 07 Feb 2025 06:54:21 GMT  
		Size: 69.3 MB (69311175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa6f387c931a30956cd2289dd9f8ee0cfb0f858bb8f13d394c75fea490333ec`  
		Last Modified: Fri, 07 Feb 2025 06:59:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c5aecd79af82c5dd49afa4698439525ad85970ddfc8b1a93ca8805eaae80ea`  
		Last Modified: Fri, 07 Feb 2025 06:54:22 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:19f60ab9c4bfc3bdfdd64f1317e1b4a3592ff86076e9715522943dce192ed165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32c062d40c72d963265395e53e2dc0acba1a1050adc412a890aef6799036e05`

```dockerfile
```

-	Layers:
	-	`sha256:55010520688215aca08a9817b1612cf70c6ac6ba6928b7dff7564b00fdd99a47`  
		Last Modified: Wed, 05 Feb 2025 08:42:09 GMT  
		Size: 7.2 MB (7214038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c9518e04a3a8346892d5b33668509af2a00896bc7eaf7475ec9dd10c3b2001`  
		Last Modified: Wed, 05 Feb 2025 00:06:00 GMT  
		Size: 15.9 KB (15937 bytes)  
		MIME: application/vnd.in-toto+json
