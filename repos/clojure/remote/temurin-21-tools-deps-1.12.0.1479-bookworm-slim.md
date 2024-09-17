## `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:3abed873e8605ed7af2ffbe1b4503999140892021bceb589ffa778e0a52a2842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ac1e47d233238a285ec77ffe986b3f3759563044ba970b64c547b4860c238f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257189627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5278228045b5e6a6e07250d4707e848697a3f8279c8e14a0c1898566c8e29cfb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19dd760509d6990667dfdc39eeb5576f4fce45ad9933b660e462622fc98dbd`  
		Last Modified: Tue, 17 Sep 2024 01:57:08 GMT  
		Size: 158.6 MB (158579313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63260fc08d4ddaa955e915e132eb9a49d0b39d3e8926e62d972d049ee7e56aef`  
		Last Modified: Tue, 17 Sep 2024 01:57:07 GMT  
		Size: 69.5 MB (69482784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748c2907f02da301685014cbce94872708a6608c5e555d1d2d39f7e09fe9b77d`  
		Last Modified: Tue, 17 Sep 2024 01:57:04 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5650c38a7251bc9138f00c615e805b2a207ce30e556a874d75967adab10c6b1b`  
		Last Modified: Tue, 17 Sep 2024 01:57:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:597553fc03cd02b6c65342724ac4598b8b0a8eb0fd697c8532fdc8a5a926d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4762107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a05d2f3648561c4da1e6e6ccab6ba4fc1950ea33cf6155357a2cce2fe5d357e`

```dockerfile
```

-	Layers:
	-	`sha256:0158e984466296c2bd3202b47ef5f66427c3c22263ae14a43aa37719802147a1`  
		Last Modified: Tue, 17 Sep 2024 01:57:04 GMT  
		Size: 4.7 MB (4745898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ad7bed88a1247a632901f71bac5751c425f4d09e2e19822003cd164bb32c4e`  
		Last Modified: Tue, 17 Sep 2024 01:57:04 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cfb0a5563c98592b67e56ae98d3dada4663587ed37b4049d95a4fe642d082f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255248395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674650ac692c131236e80be2b8016bf1c3b73cc3b51e64f2c12f3328f9763014`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2852185c1f9892de54ba89016ebfc06a6aefd5aa5906fbac5eb84e6d025cf0c9`  
		Last Modified: Tue, 17 Sep 2024 04:42:09 GMT  
		Size: 156.7 MB (156746196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef52e8ceee47906689e9a4389c6e552a9095f14b8263bdbc5fd191b23405e6`  
		Last Modified: Tue, 17 Sep 2024 04:47:47 GMT  
		Size: 69.3 MB (69344609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33518a6047e02f05fad0206db6b9fed1b301bcfc7e5959b32ac3008284b3c186`  
		Last Modified: Tue, 17 Sep 2024 04:47:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13785fd7cf1263f89e07e331338aaec1f5b2989431d78ddf40806cdf2e15eb0`  
		Last Modified: Tue, 17 Sep 2024 04:47:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:48f1c01737bdc327807b27dbf4a762b0e22f3661cb28e272054f0291a5d9eb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4769081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e4c100a799daeaee10186486e5c61a888118ccaf3d99f979150af14ff05d71`

```dockerfile
```

-	Layers:
	-	`sha256:55386e9abc3d0fcd44d3d3e2aa8708894c1dd92c397118f902c5031338c7aae1`  
		Last Modified: Tue, 17 Sep 2024 04:47:46 GMT  
		Size: 4.8 MB (4752307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6126ccd363695f5d69facdc7d50aae232d31e227ea3cc025d6a2b014772d662e`  
		Last Modified: Tue, 17 Sep 2024 04:47:45 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
