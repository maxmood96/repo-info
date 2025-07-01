## `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye-slim`

```console
$ docker pull clojure@sha256:c33dabb380c09d4364ce8a6aab1420445779e6ac60c1948c8647e96d8ca8811a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6bc04a539402a0c6914930e5d7083a2beb4030f1ab68752397f90fdf3507db25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179214869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979393893d26c237cd4f5f167b6eb84b02326d227085b1695ef8132c6185cefb`
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
	-	`sha256:48348d2867466dc769c153a1acec279d1b9a0d6b9dad8d405d0f14294143782f`  
		Last Modified: Tue, 01 Jul 2025 02:40:46 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9daaaa241b8ef64abfe24cdd4c37e21601e65ea966a35c2fa632c3e23f4386`  
		Last Modified: Tue, 01 Jul 2025 12:55:50 GMT  
		Size: 59.0 MB (59005783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa900d844629288fbead9d6920f99279db2dc247b06bef58eacc75c54a7e73b7`  
		Last Modified: Tue, 01 Jul 2025 12:55:46 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa336eac294ad0d0c3feb8426cd6af52a19b350a44e23d0d2be4c3c86c7545a`  
		Last Modified: Tue, 01 Jul 2025 12:55:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f6437c37d28aae8b6a4b65292c52ac74dd31b6ec56c4432c85abf3c3582d4d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830d534ea0d1118220951ce3e0fa82d223af0be0ba53fcc0b58a07577923f129`

```dockerfile
```

-	Layers:
	-	`sha256:869525adb4dcf13509dd8eeb63cde4c55edf351f9e71dc901267ed465a2de432`  
		Last Modified: Tue, 01 Jul 2025 06:40:26 GMT  
		Size: 5.3 MB (5258684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4bf1a09bf77a32bff652aa4b9b58656736b70dc5a4d2775d6a7db18affae8e5`  
		Last Modified: Tue, 01 Jul 2025 06:40:27 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:31d7e315e79d97f37cdcbbdc6e1320707184a78d989e1ee33a3aa74b65194731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176973917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d007a5e088582cfe55a218364dc457ceb81465e865893ef77b7f8711082dd2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578690a96e2e4ba5fbf59b73b69955c75b8c7c6c842e0231034a946fbb7c86d0`  
		Last Modified: Wed, 11 Jun 2025 08:45:53 GMT  
		Size: 89.1 MB (89091276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff363b88eb63e6f24274f12213c798a29b4e5199d4e449e8babc6f6bc28b798e`  
		Last Modified: Wed, 11 Jun 2025 08:48:51 GMT  
		Size: 59.1 MB (59137417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240c55fd9ca18700ab0a62226b0a15cfcc59fe3c3b9681da0551b9fca492db98`  
		Last Modified: Wed, 11 Jun 2025 08:48:48 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d981fc5f187e13d86339879ca23c74a21be83659b6a68f729aaacf5ff068531c`  
		Last Modified: Wed, 11 Jun 2025 08:48:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:afb64f43d94bdd1f7f50bf630deb1a8f6b046cbe23f2869c0e2058ffa45a7728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aac6a1fef6befb7e0bffdc19abbff922d1003b325bef727c2ce14836a9b5bc5`

```dockerfile
```

-	Layers:
	-	`sha256:170f588293d383c92bae1c3480970b9cfe330062d1c480129cde043b2d2e1221`  
		Last Modified: Wed, 11 Jun 2025 09:41:01 GMT  
		Size: 5.3 MB (5264413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7192938d0892a1c72923184f9d7ec2faa0726c6b617327c97611cb962d0e1ae0`  
		Last Modified: Wed, 11 Jun 2025 09:41:02 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
