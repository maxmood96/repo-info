## `clojure:temurin-24-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:4f97e50c29d6b84cf73430881587c40d860c768b47fc730206e047210606bfe3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:173935897772ab63959bc4b4f1697ac89314d71975360c228b2a5220adce39f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219434520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386c7a4ba3342437f4b473a59bcea4deb8a88bc4e8ea7e37370ebd8c9d9c69c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c7be967748db1deb3f5da8beb1bb895286c6537627e1c7ba541382372ee761`  
		Last Modified: Tue, 08 Apr 2025 01:36:54 GMT  
		Size: 89.9 MB (89949049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328a08b39171d34ce1e6338293a17e366855f4a86dcc007df6cb346be44a1bc`  
		Last Modified: Tue, 08 Apr 2025 01:36:55 GMT  
		Size: 81.0 MB (80993891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833ff02204b1d63538dfaed3593cb5a3d2c541ab041b44b9474516a617176328`  
		Last Modified: Tue, 08 Apr 2025 01:36:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3965fc47bee9a257f6e677ba9f5c4189d42749d9a5300b01e21c3221c9fa4c`  
		Last Modified: Tue, 08 Apr 2025 01:36:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dc384af9b9d464c3ade7088217ea1ef32e1ff99b9436493627ea7874e70d2e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7140290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75eba903d144609f3301838201f4577623c15e922a346eb27288c1d1233a0bab`

```dockerfile
```

-	Layers:
	-	`sha256:068f173d029d769f1d48f5cb2c5299656112efb973462dd8cc09cafd098af00f`  
		Last Modified: Tue, 08 Apr 2025 01:36:53 GMT  
		Size: 7.1 MB (7123792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a36b9fa102ff07aa2aba3e36b992f59553613fb57d34441057dab20787eed6c7`  
		Last Modified: Tue, 08 Apr 2025 01:36:53 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:074f3496836ec44b49c5264d4f32c13e25637955e723c45c211a61d6416ff6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218263727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd367bb511a2f8cc199d08c0f73cca414ca9bf60f13b79072f19d4cd95afd63e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056da6c0260d4ec3328806ef52e521e6ccd120e28592a75f2d7011ea55faf71b`  
		Last Modified: Tue, 08 Apr 2025 11:37:08 GMT  
		Size: 89.1 MB (89092720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19585910ed355a32971353e47f4d6bc79dfe0b5fc68140aa4efc7f7d5530f5c1`  
		Last Modified: Tue, 08 Apr 2025 11:40:20 GMT  
		Size: 80.8 MB (80842494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e19d689e3d61007a90ffdb9fc99cb9ab51caccc8ba773054b5ff57d369538b`  
		Last Modified: Tue, 08 Apr 2025 11:40:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ba507ef3b55ae1eb7b9f2a9bd8b02440b0e9aa581ceb90ad04b3f87281f8cd`  
		Last Modified: Tue, 08 Apr 2025 11:40:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:957f7630fb14f806990ecaba115406fa3b65f875cf6a01f730aadc6b09051aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7146216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe3cedd29e0dc41fa4c4cf66e4ce14d3d1474f0ed3af7cfa1db091fe12dd7e6`

```dockerfile
```

-	Layers:
	-	`sha256:e0a9f847c33ea5fc32b0064a525bd8c733d874a44029be239e3ffbe4d4d2b126`  
		Last Modified: Tue, 08 Apr 2025 11:40:18 GMT  
		Size: 7.1 MB (7129576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d2e50a7464cb895ed3df360bcb67496d43243f03f694fdd52491907eb18233`  
		Last Modified: Tue, 08 Apr 2025 11:40:17 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json
