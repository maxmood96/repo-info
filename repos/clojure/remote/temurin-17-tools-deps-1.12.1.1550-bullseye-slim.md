## `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim`

```console
$ docker pull clojure@sha256:439e48732b29a60f2f1c90dd1353e2cb0104012f55d7e4068e2f04c318531a84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fe8a0e0d424d80bebbe7889ebab79d88bcde27fb2f2095ffe2cfe72cf02e47c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233897672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0273bf3fbe8040df67b01727a6d05f148e6ba8c196258ead7b5cd50d1be8be4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89892b989d441d98f7a564857ffafd5632c0d6fa2aa22fd18ccff44a9caa593`  
		Last Modified: Tue, 01 Jul 2025 02:39:33 GMT  
		Size: 144.6 MB (144634948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ec713b7515cbcf2d67fd13d11ec9d853ca00833b39f83c1c58b91c9dbdb2b`  
		Last Modified: Tue, 01 Jul 2025 02:39:45 GMT  
		Size: 59.0 MB (59005637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e71b9e6890c90e200082771d73ddea2c24be91d3d554427ddab9004e9cd450e`  
		Last Modified: Tue, 01 Jul 2025 02:39:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2ad657f21446a9b69a2d2e1612c055f593412f3c4ccf532eb491fad6861af`  
		Last Modified: Tue, 01 Jul 2025 02:39:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c2f6892026c3bbe3979190af97d327d3f25d6ebf3e5a95b271f6b58a25db51af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ea4828a4a87b8fad3f147e0b0cec02f5d5b81dc36cd0b3277323ebd8d57a1c`

```dockerfile
```

-	Layers:
	-	`sha256:4cd2a4ebcd1d219d0ae06e64b866ed5c4ba76feec31765923691dbd6cca6b8c3`  
		Last Modified: Tue, 01 Jul 2025 06:37:07 GMT  
		Size: 5.3 MB (5308038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5685c82944b6ff835d8cdd0c18762912160c3124ca988b76a52e27bb00100cf9`  
		Last Modified: Tue, 01 Jul 2025 06:37:08 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:09131d9ded1ca7bb2cf0bf6d3845bdefb240fbf1e02e0f05fc0aab4819368405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231395541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a326c42e2b5530a835f44f4037f0d56d01875efd6a1a81a0fbb4c5595bf7461`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62bd73b5d8c3ab8e527ba51e9b40ba5e6501a7c7901b0c2ec811446b945e8ac`  
		Last Modified: Tue, 01 Jul 2025 08:50:41 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b885949bf96cc931265f7bccff494ebc4e2802de96b38a780f693ed054fc1e7`  
		Last Modified: Tue, 01 Jul 2025 12:26:10 GMT  
		Size: 59.1 MB (59137727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ece8d63dad626039ae252d4381fbace7565177528551e431f8226d7d51704a`  
		Last Modified: Tue, 01 Jul 2025 12:26:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8730c9663c266dbc29e111bf2ff925f3a2b043900c90a2c9348d75bbe18730e6`  
		Last Modified: Tue, 01 Jul 2025 12:26:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1c7422a8d7a915faa3325d04f6c4b70b140555ee26af026acc9092eb61d07575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef1cec9370e8bbabd9ed03d05678af5ed423d717e59ae599019f9d4a7f69050`

```dockerfile
```

-	Layers:
	-	`sha256:49d9c907e87bcd15acc395beea759fa5aa90e5df710374f6d8336bb701bb1460`  
		Last Modified: Tue, 01 Jul 2025 15:36:51 GMT  
		Size: 5.3 MB (5313770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29402321115e6fccc09b5ddc4c12ea4ad06c7c4e607619ab04d28e0cb1572ba5`  
		Last Modified: Tue, 01 Jul 2025 15:36:52 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
