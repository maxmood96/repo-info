## `clojure:temurin-17-tools-deps-1.12.0.1495-bookworm`

```console
$ docker pull clojure@sha256:7a9880477675d11b9f1b2237997ce790bd9c41687b5b443b169e20157d4d83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1495-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:81bd115be8c64d9908ca53b7e20b83fcfa8612d3c0ac9d8539d2fbce258915d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273810917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349383526cc3299a0291ab9d97ecc419e34afefcb2d26eea92de93dd4b4c5c80`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603fefbdd17997413977a84544da923cb691f54422f3210e600a92acf7b38b05`  
		Size: 144.5 MB (144536674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f23e744e94c9743092ef41f951fb72011bf2c77037b21fc9cc3ecf8c883ce7`  
		Last Modified: Tue, 07 Jan 2025 02:29:26 GMT  
		Size: 80.8 MB (80776140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0a604f3e745b00ddcaed5724bd463d5e573eb79008718bcbe736b5985f9b1`  
		Last Modified: Tue, 07 Jan 2025 02:29:26 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e606d06a03e7c2c280263ff7153138f120bdffd5ffa8fd573155ab69b1a9f8`  
		Last Modified: Tue, 07 Jan 2025 02:29:25 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:85ccf1c04c833056f897bf3c594ddef177c655f5c7b183a92a9ab1dedcaa3706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5416ec5ffa59870a1b95508bfad6d2bf2d32d1a41657da765cb980eb3b7dcd1`

```dockerfile
```

-	Layers:
	-	`sha256:6564d4b872b2a493e12ea35660854a2ad2c6400fc3c8a113142831aa0bd8c77d`  
		Last Modified: Tue, 07 Jan 2025 02:29:25 GMT  
		Size: 7.2 MB (7171080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ac269d9e5ef6a146fc18156b03f99ddf68a401ba69a1c5e0da03edeb8f6916`  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
