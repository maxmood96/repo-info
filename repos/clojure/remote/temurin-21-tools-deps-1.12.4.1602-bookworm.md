## `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm`

```console
$ docker pull clojure@sha256:4affdac62506bc501063853e5ced33534249cced9c9fdb18f6ea282efb9943a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1dda5847d6b680a29dfda60570b5aee9ad52385f40df7fc85974cbbbf6a32cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287490105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc40fa8afd9fe98b42283d91139b4a65e340baa2461256485cc6c518107b0e6b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:34 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:44:34 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:44:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:44:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8185825c64ab474812159cc8160b57fd6425f9c151ad94567cfb9abb929355ea`  
		Last Modified: Tue, 17 Feb 2026 21:45:15 GMT  
		Size: 157.9 MB (157857066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cc120db5c077a49ae82f32c867f146723f030e14c2e37f4f04cf4266288212`  
		Last Modified: Tue, 17 Feb 2026 21:45:13 GMT  
		Size: 81.2 MB (81150513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0f8200b9cb1166e2216f5b37b0179e2b24c6345d46ddbbe5868ed6fe1a057f`  
		Last Modified: Tue, 17 Feb 2026 21:45:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df6b57940e4159a36051d84ba67fa8f5315136f33351759b150c8e93328e066`  
		Last Modified: Tue, 17 Feb 2026 21:45:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8b81d6291d50e625f939f6527382ae44aa6482d2e47b7234dd8d2ec33e677760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5803199ac6fa78f5241fa8a796538a55c01af1c3aaa8555544fe2972e2c033`

```dockerfile
```

-	Layers:
	-	`sha256:f01ff3c802f2e4db75f32250f022002f261fe8ced0306e02a166f93bcc5b8229`  
		Last Modified: Tue, 17 Feb 2026 21:45:10 GMT  
		Size: 7.4 MB (7379325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57fec235dc8484958f19bb653dd654de3ced372cd3aa30f3bf524af3b2b38cbd`  
		Last Modified: Tue, 17 Feb 2026 21:45:10 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5cd535f92f7cb1845f6c77acafc1b7b95772206a76c9134c584bf6d18d4789af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285638480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85529a67309d398db4fe35f00cc9406b68dc15692868328d701109bcc70cf69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:44:18 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:44:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:44:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71ec52c24647668ae288ed36da41b01b3f3f97491b43f3316e57891f72ec6d3`  
		Last Modified: Tue, 17 Feb 2026 21:44:58 GMT  
		Size: 156.1 MB (156133063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b25e956bda9862c9b89a986eb11b8b67d46ff76c6a5c74d5208327c9a8a4607`  
		Last Modified: Tue, 17 Feb 2026 21:44:56 GMT  
		Size: 81.1 MB (81138419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51282a72acf48c9289d28d8f68d24817131bf77ac8024decd98a9451dd1a60b1`  
		Last Modified: Tue, 17 Feb 2026 21:44:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce207f20ec9e002b122bee17bb22ea3cedf1d1bd58bf4b6e59a30e68635b2300`  
		Last Modified: Tue, 17 Feb 2026 21:44:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e689c732714deadae3afe36da56f466afb4f5b081acf4badcc228af5500ada23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28833c8a24ce06de69bb085f6dfe7586b3ba242d7cdc7dbdfae25a5a88077e95`

```dockerfile
```

-	Layers:
	-	`sha256:b231e7a6ae3850943ce013a0d6473c6ebde0d68ffa1c938a2f5696aa131f6332`  
		Last Modified: Tue, 17 Feb 2026 21:44:54 GMT  
		Size: 7.4 MB (7385112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56b81d527a0deaee9788fdf0a25cf8f8d6d68ea00e3643c0ff7d7b683accb5f3`  
		Last Modified: Tue, 17 Feb 2026 21:44:53 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3594f0cd3d8498da4c410d2a7e492a6af600db52be7c2a0cab1bcba56f232957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297292941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043b57a47cb46580e87de3caa01cba610b43a29787e833970fe4b3a0f8369c40`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:34:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:34:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:34:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:34:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:34:00 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:41:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:41:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:41:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:41:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:41:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04686be48d2a894920edac0c0c6434c05a7128013df9522a975b048c103c93d`  
		Last Modified: Fri, 06 Feb 2026 00:36:06 GMT  
		Size: 158.0 MB (157977491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563ee00175dff89e342e9299356ae478e81ca394a247a61c2668e6d4d5a094a4`  
		Last Modified: Fri, 06 Feb 2026 00:41:58 GMT  
		Size: 87.0 MB (86987116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02f156a5b9e3d97c83ba351ed6f7ac043e2fa92a3e08eabc95e2f5d6eee89ce`  
		Last Modified: Fri, 06 Feb 2026 00:41:55 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e920bf0f293d88423d1c643976512bb472450b1dd8e4f64f7c59eae0376ab4f3`  
		Last Modified: Fri, 06 Feb 2026 00:41:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:934fec4a17685b03f9687a4dc08f44e31290224fa8353e92c091a4bbc634d736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e884b1738899f776ba80cffc28d38301a5d8b1ebc1bcfa41a617a14299fdefc`

```dockerfile
```

-	Layers:
	-	`sha256:c67e5415aa8ba7b167623375f77299806bfe62df447da3aad5c97b2317e515e3`  
		Last Modified: Fri, 06 Feb 2026 00:41:56 GMT  
		Size: 7.4 MB (7384553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d1f76d5e550ef7ad37e90f071c56e740b96fe02063bf5d167ca30463179fa`  
		Last Modified: Fri, 06 Feb 2026 00:41:55 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0cc35ffab0d789035f21b94dda2202e679e158bfe78d85621b0a3779f3f55a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274207578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db498030ac2f2b73ef6e0fbbbf7f2f0d1c9fcb6bfcae7c93fbba1c4e0610dd7b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:06:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:43 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:06:43 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b87516b64b39f17ace7ef42f2534985c89459dec5eb2b0d78d5e5ea2b52e133`  
		Last Modified: Thu, 05 Feb 2026 23:07:32 GMT  
		Size: 147.1 MB (147105286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7bb380abf1a95b9ba847fff28f9df7ef8f1da904fa04a60304281d8e794642`  
		Last Modified: Thu, 05 Feb 2026 23:07:30 GMT  
		Size: 80.0 MB (79962909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de31f432941fdb774e9ab125bf1dd29f34fc3bcd2bdc51caf4fc3b4cf7072ab7`  
		Last Modified: Thu, 05 Feb 2026 23:07:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c5b969fca9610900da426962afc4359c0d906dbb0ecc8ca1322d5ed38f2bd5`  
		Last Modified: Thu, 05 Feb 2026 23:07:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4642e16d4648fd5d8ed13c479cd6385431ec889e5a123964daa278685105176f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6949423abf2f2a9065eef6e34b247bd99e52641b046c45e21fc15133944e9c08`

```dockerfile
```

-	Layers:
	-	`sha256:2ca028c9918cd997e56d3c7f5c1540c11d452d7b0f8815b7d542cb42e030a5b6`  
		Last Modified: Thu, 05 Feb 2026 23:07:28 GMT  
		Size: 7.4 MB (7370644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acf4e3ffcb92bb36ad5d41be16054ccdc335f27e1d7ac809d1d9a915afafbf18`  
		Last Modified: Thu, 05 Feb 2026 23:07:27 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
