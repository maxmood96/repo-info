## `clojure:temurin-22-bookworm`

```console
$ docker pull clojure@sha256:091ab55675e90cfd6bd25e8e2f4312fc479acd5dcd131ba24618a8d06740eaee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:e623e775bf3d26bdd5a30d7dd729e844a342ea4aef764aa14c9c9b23ae94213a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286550713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0876b6124f5e0b41c8f68c56efd5e60924f3c59de4bf6fdba3acbd0ff1e2b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a5ba0901fdbddc420a57764dbabb8a07076ee216cb712c54cc3f00770a6391`  
		Last Modified: Thu, 25 Jul 2024 19:05:44 GMT  
		Size: 156.5 MB (156481615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27e1f75ba7fbfd5e340b65856e78c73c82dccce10e69e01287469c4d0edd262`  
		Last Modified: Thu, 25 Jul 2024 19:05:43 GMT  
		Size: 80.5 MB (80513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75dc79d0f1f4e20db12d8b8cfcb5229780e2544828f3931bfc2998e999e0b89d`  
		Last Modified: Thu, 25 Jul 2024 19:05:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e696323a24772fc7a5e807e706958d5502bf3c362d0fe8d44495c1866c754294`  
		Last Modified: Thu, 25 Jul 2024 19:05:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f30d7ad5e17502a986655c9d6942f726cf9ee77505ec54bd9f46ad126250764f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1e00f1cb68bdc59b7ba93bb24d444c9dc7399c7f849e049362dd08b08469d8`

```dockerfile
```

-	Layers:
	-	`sha256:cb338fb3e508dd694feffc151d4e5b368da371cabbbc9d7042553853edd06f03`  
		Last Modified: Thu, 25 Jul 2024 19:05:40 GMT  
		Size: 7.0 MB (7000764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ecd2a3334c13b8ac439cbf2622957f7d40192163e7b401a7f684e5da4441f1b`  
		Last Modified: Thu, 25 Jul 2024 19:05:39 GMT  
		Size: 16.1 KB (16124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08c85bb449890e4b4a719d15e125ea6696ba01aebef9003c40fb989ae8a61e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284352205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab48df279fa790ccc79b364fb8f998655c2086a77ee721dc9cd2079dcbb628c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:19:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jul 2024 20:19:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jul 2024 20:19:09 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Jul 2024 20:19:09 GMT
WORKDIR /tmp
# Thu, 25 Jul 2024 20:19:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Jul 2024 20:19:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4c9a1a0bb41bcc3f3a8491c350442160b221aa7c51caa60ace0f14d32c1f18`  
		Last Modified: Thu, 25 Jul 2024 21:27:19 GMT  
		Size: 154.5 MB (154503755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db248057ea316732f6313d1131dd381dccbd5762776988f6704c5e7accc2020a`  
		Last Modified: Thu, 25 Jul 2024 21:32:13 GMT  
		Size: 80.3 MB (80258966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f4cc274565525a46589883b62e5d72d7197ea8c82c0d86c5ddfbcc9170a54d`  
		Last Modified: Thu, 25 Jul 2024 21:32:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3635aa76c44621955d53339db6a5b267ec18ef535c95bbf68620d5dfc84ba9`  
		Last Modified: Thu, 25 Jul 2024 21:32:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2029e464930f14659bd2f9e9d5c1b12a3b156d9926fd6b95fb9efa30cf82697f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7023859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db19038b346ca0a007139654286a0abd3e409e34cc9d15d8dfeefba4eb6c37d3`

```dockerfile
```

-	Layers:
	-	`sha256:d04e48a5fe0fe4853e080b1b4a890904e345e0d4c100f05aff1ed795e68cac1e`  
		Last Modified: Thu, 25 Jul 2024 21:32:11 GMT  
		Size: 7.0 MB (7007175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14aa26b2c9b573eaeb71dcb7be25c99fc7c0d9916a83ec4d40162edc6d894aab`  
		Last Modified: Thu, 25 Jul 2024 21:32:10 GMT  
		Size: 16.7 KB (16684 bytes)  
		MIME: application/vnd.in-toto+json
