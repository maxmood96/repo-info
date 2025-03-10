## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:6f09dba5f49f16928f1fda235b16c4f5325a6d89bea0aa32073a8a29c0de3658
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7cea85e4a28c0c3742cea43f1ab5508adc7d8642bb348aab1e0c380124eb5629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242314425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31962d41dd5bf07e177229ee6b63bc24bbe1c20ccc6ee196eadf06ae41a8c536`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b2398a85f2e93f74dd9d8f4090de06bb6bf3e9961f425db269f620cd870eb5`  
		Last Modified: Mon, 10 Mar 2025 17:40:06 GMT  
		Size: 144.6 MB (144566550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8472e3eb6597d2179e5b068c12b2888cf348f226aac21559a6bc40872c7ba81`  
		Last Modified: Mon, 10 Mar 2025 17:40:05 GMT  
		Size: 69.5 MB (69527532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27520f6d9792094904fda922325f7aaf46695912a7f77c199a051fdca43eb818`  
		Last Modified: Mon, 10 Mar 2025 17:40:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee7c977d8dc29b7aa0a333779d46fa2723596bad9a5f3410390c154667517b`  
		Last Modified: Mon, 10 Mar 2025 17:40:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:446f3fbd1dc5fdf2055a19f6208e58eab22576dca2cca56586ebaeec5d556d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b89d56803d6544c4862a7edefcc56ecc015d22c37e205a4ea390d1f44b5c447`

```dockerfile
```

-	Layers:
	-	`sha256:871ba35c2f0a309a05340b6545f5f2ae95c887f8ea580ce9be596b4c6b924743`  
		Last Modified: Mon, 10 Mar 2025 17:40:04 GMT  
		Size: 4.9 MB (4912585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17eb47692349ef3e3cd032e1cfed061455b194a06a449d33d37def8c29c89275`  
		Last Modified: Mon, 10 Mar 2025 17:40:04 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f771e52fa7ecc838f064c6c6fd8f94a7712279fcd20f04bb651326208ca138d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240882690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72174b274125c2182dd6b6f75c32a8937bcc2858b5c2e13335c65bfa055a383`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023fb8ddeb74577aff364f9176a4e554f3cd037752f74cbf43d53f0714c39236`  
		Last Modified: Mon, 10 Mar 2025 18:01:03 GMT  
		Size: 143.5 MB (143454722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2778210d1d31e6d24bccbef86b80b291b63a5e8ce4e6b271ff8e0e9d268ecb`  
		Last Modified: Mon, 10 Mar 2025 18:01:02 GMT  
		Size: 69.4 MB (69378496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3ff78e45cc346fab504ea16b3acaf62147aef1c625a1a1a88ed8071f29e02f`  
		Last Modified: Mon, 10 Mar 2025 18:00:59 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ca5facae939572db1bd8075d0780b4a5f61438a341d65473067ae9c9edbcda`  
		Last Modified: Mon, 10 Mar 2025 18:00:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f5ea3bd85c5bfff95f491e4726707417d855baf67dd38c5cfd437789baa7794d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daedf3100b994bc2ee8bf3ea66df71efe7c36ee53517844e9a7adf990acb2257`

```dockerfile
```

-	Layers:
	-	`sha256:baa09e6141c6b8cf4a265f7800a8c30df0e3c5908fba3a1a1595b090ff8f88c1`  
		Last Modified: Mon, 10 Mar 2025 18:01:00 GMT  
		Size: 4.9 MB (4918346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ed7f71df313ada77130abfee4129ce715f0b8dbd3a15d6eab6cb405c833708`  
		Last Modified: Mon, 10 Mar 2025 18:00:59 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
