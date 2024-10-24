## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:20d7919ef27cb5d250ccd6dece8143e7d6e074c83106806d8edd54050e1a9e9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a52265103d42a3a144d13e432b2648e233fb3d8f13fd014a795c414fa2a444af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288053016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f2abe7f16c86533d56c7082e8dee8ae898175aae2c991e47c9800bd33d5033`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d60fa641d3052c24cfe2bc56634299d6b6c2d92f4b3c4378f0eda2eb8cc82b`  
		Last Modified: Thu, 24 Oct 2024 02:01:07 GMT  
		Size: 157.6 MB (157568701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca21b21a9be17918a0916a74d3a48cf7c498abf81fad76c2f41588a33a674f95`  
		Last Modified: Thu, 24 Oct 2024 02:01:06 GMT  
		Size: 80.9 MB (80928250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2a919b930c5c7fe9c74c6a968c61d3232aa999dcf006b6b730533178da4725`  
		Last Modified: Thu, 24 Oct 2024 02:01:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45e42e7877d9ff951458e143bfca75d6d81aaa9104a3efd8b3e5cff14030b45`  
		Last Modified: Thu, 24 Oct 2024 02:01:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:624fb1f44dff857561c33a5c80c07bbba658038151a35b9cba4d7e73d6576284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff66df8581be80b075f9b0164c841dab86a3191f96ddda27b833418a1b49d5a`

```dockerfile
```

-	Layers:
	-	`sha256:ad683b2e4f48b8d6ed0f4ce302a2ac32281d281f24c603d5a43e6e8f8dd3a3cd`  
		Last Modified: Thu, 24 Oct 2024 02:01:04 GMT  
		Size: 7.2 MB (7187494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a808583dc4428aeca4bbc68d7dab127140f1a623bdbeb7b60f631b9234fd30b9`  
		Last Modified: Thu, 24 Oct 2024 02:01:03 GMT  
		Size: 17.6 KB (17646 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e27816a80cee76298bb9a20404a6e84c704845fd425fdb32e28159190ea8c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287122266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e7ac5011b906f19dffb482cd5e6d9c34598d54142c955cc0b42556aa9ec13e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6081bef755cabe28916d335d34f5e5bff03f6905db8f85e9e22d2927f98411a9`  
		Last Modified: Thu, 17 Oct 2024 07:54:30 GMT  
		Size: 156.7 MB (156746192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e21c332a61721f87a6ce622518a613e108366928b4035a527c56b208c9deb74`  
		Last Modified: Thu, 17 Oct 2024 08:23:01 GMT  
		Size: 80.8 MB (80790054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23d5f751a68fb74937aa3119c1af668be06b9617c105674a47cd29ca20e2a0f`  
		Last Modified: Thu, 17 Oct 2024 08:22:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b4c59a9ff684bc17cd35bc69a34b1a24a94cb1b5876caaa02816677dd2446`  
		Last Modified: Thu, 17 Oct 2024 08:22:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0457f5aa5d0ef0c35d7aa3352ae3e9f2966eeaca40ee29ade2836daf92c3e782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96610469326f010312ac2976080d4f7673b49a3c148ed96ce3db22c6eaa67621`

```dockerfile
```

-	Layers:
	-	`sha256:ffd7a791ef50a8c137605ebde7b110ec6ffb10fca6c4683d8c4fac7fb3201e41`  
		Last Modified: Sat, 19 Oct 2024 12:15:10 GMT  
		Size: 7.2 MB (7193332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f18595b0c9fdf2426ebd015e6622ba43a7e6dda92990894116ad1d8f18378c`  
		Last Modified: Sat, 19 Oct 2024 12:15:10 GMT  
		Size: 17.8 KB (17830 bytes)  
		MIME: application/vnd.in-toto+json
