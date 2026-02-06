## `clojure:temurin-25-bullseye-slim`

```console
$ docker pull clojure@sha256:fc0d28292032b4c07a793bea7e2dc5d8a724a2b953aeb2b4c84daa9eb102003d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:18c7cf447f1a14c10b2f957fe30bef49dbe81efdbd74defd0574570347822401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181652105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1eccb10c4f4edaf3e4992c9a51ae8bdb372f6ece2caa885ccf105977aadffa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:07:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:26 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:26 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f849f6fab95a2fae2e243609862b99fe205cdea0cebbdfe822150caf8290d2f8`  
		Last Modified: Thu, 05 Feb 2026 23:08:01 GMT  
		Size: 92.3 MB (92256283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc1e4bdf3cecc87dc0533562b4fa0ee9497dcf81513a351a84f6ca51fee5b73`  
		Last Modified: Thu, 05 Feb 2026 23:08:00 GMT  
		Size: 59.1 MB (59136497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523787bf9ff2107993d283f94061d68698a3b229c92c4c761bd40d2bd8950aad`  
		Last Modified: Thu, 05 Feb 2026 23:07:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278c04cd526f64f39e91a636547dd0caf6ab9b160447effb483697231c8069ac`  
		Last Modified: Thu, 05 Feb 2026 23:07:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fb6afa6282acabe09cf182b46d211f6e0f1d9d72850a1f072b6088534ca82e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4667eb0287a5aa1d2e185195eb0095e5da04cc119ffbe6ee595bcfa050e0ac`

```dockerfile
```

-	Layers:
	-	`sha256:b2c18ac64dcdb7b77f32eee799caf4d5a4a13b108d2de7eed8c4b990af36af40`  
		Last Modified: Thu, 05 Feb 2026 23:07:58 GMT  
		Size: 5.3 MB (5278214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f68050cc2af71204748029ea83c4d6f2839cb06932d5283b492a550b390cf3f`  
		Last Modified: Thu, 05 Feb 2026 23:07:58 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:90802b7808008bad97358799b4359f95f962ca95d071f4103f2c0f8d276c7e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179321884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7102a0539108774d5d98d82d90e53ce16660431b5d78ccbc7add7305455b7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:08:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:08:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:08:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:08:38 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:08:38 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:08:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:08:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:08:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:08:51 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:08:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89956777ed17e1df9f4f18ab5296ff732773219b2dff8a110103aac4eaaeefee`  
		Last Modified: Thu, 05 Feb 2026 23:09:12 GMT  
		Size: 91.3 MB (91288272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f93ad4bc89883dc415d980c9ccfbde2ef704df253d518cebdba90e8f7108f2`  
		Last Modified: Thu, 05 Feb 2026 23:09:11 GMT  
		Size: 59.3 MB (59288127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a452e460c722fbb88f3291ba3278260a13609054380ec71b872d5abb507833e8`  
		Last Modified: Thu, 05 Feb 2026 23:09:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65432d9262556b7c1d11d0dd2e34dfc28fc30834a56cde7cf72d151e1a7d38b4`  
		Last Modified: Thu, 05 Feb 2026 23:09:09 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd3a8078e2f438dce29bea80869e038cbd2f753543bef58fd92583e85e37d5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f11fedae98ea04cbfd6230c712693500cede91e159c50344accdee285194ce`

```dockerfile
```

-	Layers:
	-	`sha256:6f15f48d8031c647bf842c228291962921b7302791a47dde68fe251ce35c2330`  
		Last Modified: Thu, 05 Feb 2026 23:09:09 GMT  
		Size: 5.3 MB (5283967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94b81923fdc1eab9ce61523e0149ef54d12e2599ff25c4d30ab92b2219546c43`  
		Last Modified: Thu, 05 Feb 2026 23:09:09 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
