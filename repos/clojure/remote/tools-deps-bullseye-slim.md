## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:bf85a9847be78200eccc17d6b16e328362323d5aa962cbbf95e6e0f653bf2990
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:49e0de578b6aef1fec5a45c7e37b0eec86ab7f57d94db647c805e6c6bf5f59cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248352902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3aaf9a4add366245d4ac127275a9d6ddad1c66ccceae8bd306fb7aed920c39f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334ff9bc8e3fb618581f3fbb2054c70b651a96d4784257f6673f39a1d6c5d62a`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 158.5 MB (158497961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1ae3e57b298591dcdb1af234926ee556a33ea471683a212b4264cc7935e1da`  
		Last Modified: Thu, 13 Jun 2024 18:14:07 GMT  
		Size: 58.4 MB (58419860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c1c7d8245c7b06a7aa56febebf66ef12311d7c2a88d4a872e548324b95e008`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c840b4f98730f7b692d80e64428e7a560233413d27b19b83815a63dca92ff8`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:367110f388944ff0ba004661d36a2d3a9b1d14a9d8eece1abc36bf04a3ca1870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157709f2d960777830c26aa30ddf122ea29acc665f143b9d60dccbe4b2df30a5`

```dockerfile
```

-	Layers:
	-	`sha256:ea7d3cd6f5b6b5c5736a7bd060e5a1b8c2820e331dcc7c954bf6457d8ada2421`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 4.9 MB (4909939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986557c362888b4c2134913ebca1309723850bb627a475a59b7217f5b3976db6`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 16.2 KB (16208 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:476af18ec09dde10cce2c8bdf1d90306b1b922e3097ad10b8e14eb767af4211f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245293715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489d45e8b12e0effffedff9ba5b1f155fc0dfee5681e02bc2d7061fb0156fc17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564c25575a74b32dc66c660031ab1490f376022bf7649dbc787565d8d624ecc`  
		Last Modified: Thu, 13 Jun 2024 11:55:25 GMT  
		Size: 156.7 MB (156665603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4395531b57b9297e6482780146a12ee3e43b0756801083f18dc44dde387bf7`  
		Last Modified: Thu, 13 Jun 2024 11:58:39 GMT  
		Size: 58.5 MB (58540090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7df60427849291e07912f0b4d52e0c6ab918ccbec5920db164d777663f03714`  
		Last Modified: Thu, 13 Jun 2024 11:58:37 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9142cd0cd47e66744a097f3cbfffe000be70f82efc865d9ee44042de74174ba0`  
		Last Modified: Thu, 13 Jun 2024 11:58:37 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4380d255625e1c9e7abaee2689d4eaa69745cabc3bee02f57e58c967bb8ef84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9049262c6963c2e659c1ac5c0d91f91c8885648224353083bef943e29c22c73a`

```dockerfile
```

-	Layers:
	-	`sha256:ef2a1283ab590db748cafd4e6b22ce30bd29ddf3cec6ca18ccad7568e6219867`  
		Last Modified: Thu, 13 Jun 2024 11:58:38 GMT  
		Size: 4.9 MB (4916319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c01cfff1e4abd4c093be53a99c139bd5130c0fff82c969eae73c11304cfb55`  
		Last Modified: Thu, 13 Jun 2024 11:58:37 GMT  
		Size: 16.8 KB (16773 bytes)  
		MIME: application/vnd.in-toto+json
