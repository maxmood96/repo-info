## `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim`

```console
$ docker pull clojure@sha256:4812c2234a5fec25c29cbbb889f65a46ed672889026e7967a18f41736062a26b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7a171d7756aa3b49a6514bab2f28ad8e77905840e711ea39cf5432a5818f357a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233897793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e541aa0f00b0c5960eb0601085abd683f1c85519bc50f560ecb1d096c0e7e80`
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
	-	`sha256:6730b76d5af51ccc3b319bcab87ceb24db7f72f319da6e8bc117cbd017d79b3c`  
		Last Modified: Wed, 02 Jul 2025 04:17:02 GMT  
		Size: 144.6 MB (144635065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0437a6d72a50606903e1825aba4c81f751fa2e4a35f0203a5c6b197b1955b5`  
		Last Modified: Wed, 02 Jul 2025 04:17:17 GMT  
		Size: 59.0 MB (59005641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a782b487c44a5e7fdd8309c8e204c9dd97d716d57e5ed6295a732ff9847bf41`  
		Last Modified: Wed, 02 Jul 2025 04:17:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364d2372c4f5129e1d22a64049bb99165cbdf9133b4d4a19d8b3e5bd194663b`  
		Last Modified: Wed, 02 Jul 2025 04:17:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ddc287f79ea1940104476542d289076d5d37b1bc1c371122015c9783ec2075b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fac210f7c247a83fd45e30d6f6f268d46454ba25740b24a296705dc9d1eba4a`

```dockerfile
```

-	Layers:
	-	`sha256:c39548e834ff3209a7b2fbddcc42ee0fa92b7b24db73edf8cd7ea27e993ac478`  
		Last Modified: Wed, 02 Jul 2025 06:37:19 GMT  
		Size: 5.3 MB (5308038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4927c3077053e4f5a4ccea63e005cecf35fc1bf6a718f6de38f756e78c4566`  
		Last Modified: Wed, 02 Jul 2025 06:37:20 GMT  
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
