## `clojure:temurin-22-bookworm`

```console
$ docker pull clojure@sha256:3c68e4c7cd33ec5c0eddbbbe4da193bb065614a1e278d2880845facc20afe540
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
$ docker pull clojure@sha256:fe53bcd087a445a3c68860ee592664bdb87bc8480cd0ece4ba7ef0ee112f8a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284352682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b391f62e16c0cb9817ba69035cd459fe0c18d7f02a85e19728772a90fbce64b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeac2efa54371de18ddb3bd79e9538a977f4e87ca85b9c925de7369c3616c5c1`  
		Last Modified: Wed, 24 Jul 2024 11:36:11 GMT  
		Size: 154.5 MB (154503734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a75051f2b34dfe23be07ac8e73a26698a73f4225c7a4fa689a71c07733653e2`  
		Last Modified: Wed, 24 Jul 2024 11:40:55 GMT  
		Size: 80.3 MB (80259462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f5ef7f426875d3b533ba528fe562d3190c8cc61d70835c398ac3db21f1e35e`  
		Last Modified: Wed, 24 Jul 2024 11:40:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba88b194b5ae57d8076dd9fcce19a288ec38d2cbb3d851ed4ed15794da03dcdf`  
		Last Modified: Wed, 24 Jul 2024 11:40:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e4e2edd1e9d45fd0ea1c8839f99b2720761d7d761c5555b7d3fbd42e34bca316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7023028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377c892a966e55e3cd984eb4761efa898e7fcc950cadf2a1f35ef7bd4d14eb11`

```dockerfile
```

-	Layers:
	-	`sha256:73e389de70ebfe5694fdd3048efdcb34eae53f3e286a71cfbfb8286fbfc6ba34`  
		Last Modified: Wed, 24 Jul 2024 11:40:54 GMT  
		Size: 7.0 MB (7007175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40ec5b9960f0c23df5a4717bafe59be6c732e36e0ac329248ed4284d586be33b`  
		Last Modified: Wed, 24 Jul 2024 11:40:53 GMT  
		Size: 15.9 KB (15853 bytes)  
		MIME: application/vnd.in-toto+json
