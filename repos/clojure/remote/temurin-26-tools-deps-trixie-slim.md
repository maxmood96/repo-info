## `clojure:temurin-26-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:7f29686717bc912a7f8860e0777bd0ecb3314dc8d6e66f3316fbe46c3574ee9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:54ab2f792a3eceb307b59d149572e31affb6a803153c2613a77af5b647901424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199209272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81dbbc31c3b67e17dd9f62eac9a3de124d4a8a6a71d2e5fa73d7ab0fc68b0a7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:08:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:08:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:08:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:08:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:08:16 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:08:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:08:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:08:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:08:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:08:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fe6f628295499c98a3bdaa0a3e082abf2a0efa0371c0a4d2dab912eed3c9a3`  
		Last Modified: Wed, 15 Apr 2026 22:08:56 GMT  
		Size: 94.5 MB (94455697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c1da8498e296a36d1523588574d57e81cddeb01cd9ee9edf0153cdbdef7200`  
		Last Modified: Wed, 15 Apr 2026 22:08:54 GMT  
		Size: 75.0 MB (74976895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795e38c52fa58ddd6d796074fab2c1b2f44ca10b9bd60973092ae9068efa85c`  
		Last Modified: Wed, 15 Apr 2026 22:08:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25c14a49aa085185df16640c49dd5da3ebbd274ca71842588fdeffebb276415`  
		Last Modified: Wed, 15 Apr 2026 22:08:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:73615416f1f4be54124ec5ffee0d7a02449a0d0331ed9084b66210dc443e998c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467fbdf8ea35fb1d33a7eb748269823452962d3f39bbae7e0f4cfe774e916b22`

```dockerfile
```

-	Layers:
	-	`sha256:1cc450dddc9ae941a2ee4b4de0a2d466eb1324420dbb783eb6b68040d299a9b7`  
		Last Modified: Wed, 15 Apr 2026 22:08:51 GMT  
		Size: 5.2 MB (5224642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bb3c991295954e2a6b777eefe03697d847fa7621ebbf0efc52ca5199aaa9b99`  
		Last Modified: Wed, 15 Apr 2026 22:08:50 GMT  
		Size: 15.8 KB (15805 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23d2f5b3e7c1bccc5d190396e08eca08f0c68c15c6c1995881413a4fcdf59584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198684124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c86ef8f8b8b9e27942edfdbc15b21bf1b1e9928dd9bd3bdd43ca99df2e48852`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:19:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:19:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:19:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:55 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:19:55 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:20:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:20:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:20:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:20:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:20:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5a511d1e08066c069fcfdbf2aa4367eed4d9d2d77c263c5296b71f2dddd9ff`  
		Last Modified: Wed, 15 Apr 2026 22:20:38 GMT  
		Size: 93.4 MB (93395224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9fc2f985c22eababcfadade7cef3fddd7eac29130d95b9e31b599892890937`  
		Last Modified: Wed, 15 Apr 2026 22:20:37 GMT  
		Size: 75.1 MB (75149308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6106ec2c01b4a836826c559c22d8c818f295907b6c9d149fb8c2bff7aaf553d1`  
		Last Modified: Wed, 15 Apr 2026 22:20:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9882989b53b1a4ffb5e045d3641f029440350575e9bdf4522da62706534d46`  
		Last Modified: Wed, 15 Apr 2026 22:20:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5cf584112eed4db803396aac9b486fe8eda54368c15c8aebf081e788d05ead36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d24bd647cc09855ba595a87bd2934be62bb0c166d193c2378a14fb1d0263efa`

```dockerfile
```

-	Layers:
	-	`sha256:69dc36e5ae4c0371dfba2618278718a591d8641237fadec9c8f51ba80cd010c3`  
		Last Modified: Wed, 15 Apr 2026 22:20:34 GMT  
		Size: 5.2 MB (5230408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174b62e35c002754f3db14589b504634d356f2271f69b28edce02ce98b6f4d1e`  
		Last Modified: Wed, 15 Apr 2026 22:20:33 GMT  
		Size: 15.9 KB (15923 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:885e9fad9902b27b753ec2579b6f3b7aefee87b093e1aebbbb346c10da9a5f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207985989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b869cae6c8fbc7787bf00ffe434fb64c444572a3821b515826541cb5c8642251`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 00:53:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:53:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:53:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:53:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 10 Apr 2026 00:53:45 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:58:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 10 Apr 2026 00:58:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 10 Apr 2026 00:58:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:58:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:58:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad9d78de109af0508c6cea77373f8cb08369c373cf24c72f7da9935301139a`  
		Last Modified: Fri, 10 Apr 2026 00:55:00 GMT  
		Size: 93.8 MB (93781481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac72e545ef7eefd4903d47a4d9541b09a6a095df7fdd043f838ec6ab97bea3c`  
		Last Modified: Fri, 10 Apr 2026 00:59:18 GMT  
		Size: 80.6 MB (80610448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5770d7433e19a249b7ef4a5e0d8e1e91476ea5cc03899e54182e4fd200998295`  
		Last Modified: Fri, 10 Apr 2026 00:59:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af421ae655820796b85429674b1042a4fbc995ca03e4412b7cc1690a2ce97157`  
		Last Modified: Fri, 10 Apr 2026 00:59:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7fb3abb958dfcd8a9cc718c35d6efa459a9534434d13a98e55a257248fd6decb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1886867b07d17a91ad194af5b409b850b325f4df8ed4f7ea5537553d32cf12`

```dockerfile
```

-	Layers:
	-	`sha256:9ac52f6a9af55208ef981b4006459f47596280aae5bfa0d8c807fcfa25073a60`  
		Last Modified: Thu, 16 Apr 2026 03:18:34 GMT  
		Size: 5.2 MB (5212949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e510e9704a8cc8ad66b9d7473efa5cc247f6c0a47a9dc9a8e5e901bd1ccee15`  
		Last Modified: Thu, 16 Apr 2026 03:18:34 GMT  
		Size: 15.9 KB (15853 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:6fb24796d4090956e75d654ea5f27811a14239f71ba679522311f75f1d9cc529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194804073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419bd355fe4e00310d8e7114e0a873ef92cab9bb60444123006a93a5b333f2c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sun, 12 Apr 2026 18:55:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 12 Apr 2026 18:55:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 12 Apr 2026 18:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 18:55:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 12 Apr 2026 18:55:33 GMT
WORKDIR /tmp
# Sun, 12 Apr 2026 19:18:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 12 Apr 2026 19:18:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 12 Apr 2026 19:18:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 12 Apr 2026 19:18:55 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 12 Apr 2026 19:18:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fc246f5e32984af9b4236c90104244f3679fa7192854d7e61221c59edbfc2c`  
		Last Modified: Sun, 12 Apr 2026 19:01:08 GMT  
		Size: 93.0 MB (93008131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4ae2605017aa1d6f33c7da5e31a3615d336382b884d351cc650ccabf1abee5`  
		Last Modified: Sun, 12 Apr 2026 19:22:30 GMT  
		Size: 73.5 MB (73519116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4553c37da03beb28ea8bf6c8ec57d0d2a20024234ab8f09c60479ba3643879`  
		Last Modified: Sun, 12 Apr 2026 19:22:19 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feed629c6b5064cb5863f27fa11ebdff40b2166b35c22e22190955ffeb8e264b`  
		Last Modified: Sun, 12 Apr 2026 19:22:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e7836bb7109a47dfe5b1959858b682458b389e1a11ea0ee26c3341909e7e34f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15972e24e11f37ed3f438143d5c6c8eb41764ea9cd813215b2d9cbc24bb3d110`

```dockerfile
```

-	Layers:
	-	`sha256:df6b1e3bf94b213db10b32f45bfd62342ae93378c1225c8fa710d1a2a381f63c`  
		Last Modified: Sun, 12 Apr 2026 19:22:20 GMT  
		Size: 5.2 MB (5196741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e9a89a1e78e2424eb9dd27af47d667fc8b7c0ce5f92bf5e1385b1d6169dcb7`  
		Last Modified: Sun, 12 Apr 2026 19:22:19 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3c1f39dec1d6d5b1b7a0b3b59633da3dfda8254cd17bf28b29332839e61b1d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195982824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84edd2105d0e009c384a1d9245ca64fd8d6cf339f4c6440a65652170e114ab9d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:46:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:46:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:46:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:46:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:46:46 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:47:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:47:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:47:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:47:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:47:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d73a2a76ddf7460ab2878123e70b72f683be95027429b7589ec35877df13dc`  
		Last Modified: Thu, 16 Apr 2026 00:47:24 GMT  
		Size: 90.5 MB (90547699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ad69d85d809c5dc4fdfa3ad7a95bef300ed6ae0e069fcf59199845beb449da`  
		Last Modified: Thu, 16 Apr 2026 00:48:22 GMT  
		Size: 75.6 MB (75598667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd544d6f72148576e8737de30d8b7f67f96cd2d1e72e451a76c262ef2781b4`  
		Last Modified: Thu, 16 Apr 2026 00:48:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004348d1b6eb58c750640697f74d1e77e555516da0e835a048b4e6312f98daa0`  
		Last Modified: Thu, 16 Apr 2026 00:48:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:780df2a843451a21175e19abbcd3e61859f56fb4d04827140ea907df2207c0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc82f280e98e2dcfcfda36656c38aef384f8a75afcb292305295c8ad840da0b5`

```dockerfile
```

-	Layers:
	-	`sha256:56431f1ad1354824ed76873607154118314d40aff6e5fe189652b2c88b7554bf`  
		Last Modified: Thu, 16 Apr 2026 00:48:20 GMT  
		Size: 5.2 MB (5205752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6f5a0ca8a549a288d7933280b667f10a4eea1d3349e77fdc1bad5a9f386fa7`  
		Last Modified: Thu, 16 Apr 2026 00:48:20 GMT  
		Size: 15.8 KB (15804 bytes)  
		MIME: application/vnd.in-toto+json
