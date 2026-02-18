## `clojure:temurin-21-tools-deps-1.12.4.1602`

```console
$ docker pull clojure@sha256:950956a10a7d15215ebd91a7cb1b684d859d52300b3701a1a62b148a25f92752
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

### `clojure:temurin-21-tools-deps-1.12.4.1602` - linux; amd64

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

### `clojure:temurin-21-tools-deps-1.12.4.1602` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.4.1602` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-1.12.4.1602` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.4.1602` - linux; ppc64le

```console
$ docker pull clojure@sha256:bf5bf98f62b86434ce07b9e7fe219f2bb0b394948c1d7998dc9ad6d559cc4629
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

### `clojure:temurin-21-tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:2a87b6e4dba034b8b05fafb44780748fea4bdcedefb4ec5d42aaf6ac5626e42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e375320b1e2805fca907af49de17330c6c3bc4832ffe37748b09e98544d946ed`

```dockerfile
```

-	Layers:
	-	`sha256:0b325c284c37ad5a0597c298a50dce60f527c6e1096d8c9506e73fe5fb6eedff`  
		Last Modified: Tue, 17 Feb 2026 23:59:48 GMT  
		Size: 7.4 MB (7384553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f23d91d9c95437c5bed2eae22570963be460cbf428d92d1d98e306fd8eb7ddc1`  
		Last Modified: Tue, 17 Feb 2026 23:59:48 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602` - linux; s390x

```console
$ docker pull clojure@sha256:54114dcbb5ecb6f57b1f81940c6db1337cf2bbc955c7e68554b664507e2d9b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274208510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c173f2c14f8e2adf7e0e19c7b645eb0c29ba5f620a9ac5e1eee190e0469afa47`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:13:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:13:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:13:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:13:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:13:12 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:13:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:13:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:13:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:13:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:13:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b838670a4f355a1ac037114110d70a67c8c7c1288cea2a0bcf49e74a0f97637`  
		Last Modified: Tue, 17 Feb 2026 22:14:43 GMT  
		Size: 147.1 MB (147105302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf40ebe17981d10019483b24c5dbf1f3edcad2edaf35b16ef338235ee9f11f53`  
		Last Modified: Tue, 17 Feb 2026 22:14:48 GMT  
		Size: 80.0 MB (79963818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af4ca1e6d77b67989dcdaa7ff5c8725e45dd4cc2abd1787e50296da24970f3a`  
		Last Modified: Tue, 17 Feb 2026 22:14:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618432aefeca4f6d066d9cfd5d19d37e2afdbb4e7195b433fd669dc6a7897c63`  
		Last Modified: Tue, 17 Feb 2026 22:14:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:0111ec2e5ff4ab237413537b6398206d105028bcf5f2d590e104c2fb7662e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c62e9e9b1b12048fc5059fa922c873fdcfc2140cf629544048a3dfd649f000`

```dockerfile
```

-	Layers:
	-	`sha256:62de151432e669d4b69d951d723ed0653f6223c281c39de196b0b47901d50aba`  
		Last Modified: Tue, 17 Feb 2026 22:14:44 GMT  
		Size: 7.4 MB (7370644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c5213e7da4e5918712510d50473ec9e07980cbb6808d838b02478c1a09f0d5`  
		Last Modified: Tue, 17 Feb 2026 22:14:43 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
