## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:01f22a922a1d729b219571222e527d030fddd8e42cf0dbcbecbde22d1c019a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:83db32b6c3a9578de857c3fb28100c4a11680777d5ccf9aa01e99c4322944398
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268952298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e4b8e35e022dfa3194abba00ccace00c357cd8329835e243d2d3248a41af7d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 14:20:20 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Wed, 17 Jan 2024 14:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 14:24:42 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 17 Jan 2024 14:24:42 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 14:25:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 17 Jan 2024 14:25:00 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 17 Jan 2024 14:25:00 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 17 Jan 2024 14:25:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jan 2024 14:25:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b5b6c19e935fceec282e83861770b734b59de4956764e9c1adfed13faa3893`  
		Last Modified: Wed, 17 Jan 2024 14:57:29 GMT  
		Size: 144.9 MB (144873945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451bffed0e608b091abfa27e98f48a70b139004a48e769eddacf4e79d8cedf6b`  
		Last Modified: Wed, 17 Jan 2024 15:02:27 GMT  
		Size: 69.0 MB (69019612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444f8cfa3306d42eb3afd8791874c488d9e0e2757818699a61756baba3160a2c`  
		Last Modified: Wed, 17 Jan 2024 15:02:19 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97746f5ff40b10841144b61f5e9f2acb9ac091f403617fd839e0c1334c7e99`  
		Last Modified: Wed, 17 Jan 2024 15:02:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:09db1d3349eda462385179480dab2a8c4c4b8bfa5e17db76831f3a22bd0289eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266542961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911a5efa3265fa80a210a461dfe70bcef71360083cde2e803261b4d565de98bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:00:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:29:07 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:29:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:32:46 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 17 Jan 2024 09:32:46 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 09:33:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 17 Jan 2024 09:33:01 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 17 Jan 2024 09:33:01 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 17 Jan 2024 09:33:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jan 2024 09:33:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0181c697a313f5492a0ffdbc55abec383164f1aa430b778987b9ebd7cc657d82`  
		Last Modified: Wed, 17 Jan 2024 09:42:28 GMT  
		Size: 143.7 MB (143681767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617f74f7da253c71920072a3d74aaecc26d8abb7410f768e386979b3c7f399e8`  
		Last Modified: Wed, 17 Jan 2024 09:44:35 GMT  
		Size: 69.2 MB (69152326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b8cd60b7b5c82cbcdbd010f894e8e83c20cf1136fe78a686ca947574591650`  
		Last Modified: Wed, 17 Jan 2024 09:44:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2cf9ba6c98835db827e8d2de347eb2a99e097f86f933d6242df3030b5c8175`  
		Last Modified: Wed, 17 Jan 2024 09:44:29 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
