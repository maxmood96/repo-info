<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.17.10`](#elasticsearch81710)
-	[`elasticsearch:8.18.5`](#elasticsearch8185)
-	[`elasticsearch:8.19.2`](#elasticsearch8192)
-	[`elasticsearch:9.0.5`](#elasticsearch905)
-	[`elasticsearch:9.1.2`](#elasticsearch912)

## `elasticsearch:8.17.10`

```console
$ docker pull elasticsearch@sha256:155f1fe90eddf40b6baf1c1dec236058bc3576023ed6285ff2225512cfa0e828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:735d39468d561bd5702100cdf9cabbeca7835ba1aa37810d3791283b506c10c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676958358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c28f992cfab3539abf4de62ce93f674236ae4f80b26835a6ea937a763b148a1`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c165c7a646160f44b8a072a7eddd03084d6965b14246606044b3d9ac3eed32a`  
		Last Modified: Mon, 01 Sep 2025 23:10:05 GMT  
		Size: 4.5 MB (4493679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806378ff79a7933a0bfb4dd44aeebb5c906eb7293a0c7050d6a443c56a40a206`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7d1e096398acae99195e6b12e4c227b5fd4171f78bf1777d0ade419fb8d09a`  
		Last Modified: Tue, 02 Sep 2025 00:27:27 GMT  
		Size: 642.4 MB (642446922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eb3109af95e8b3e351751a2e8adeed242f7d40c60ff64b53d5ad6b00f6e74e`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d726b63955ce94d5c1ee1616b05b623225aeb7442505f00c802b6bc673dfc78c`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694c7cdf811762cbd2a5a46032890a0f09b15520acb89bec463d3853f649ceab`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 163.9 KB (163937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547b637c8c7831ba72963b41998f2d2fbdb28a871b96b9a49c0cc200dc490555`  
		Last Modified: Mon, 01 Sep 2025 23:10:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d029e21ed768b0a699e644429e313ef5bd6d98ef8ae9028c4eca89ea7a7198`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 115.5 KB (115542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f0839b20933ec40f479baeabae360757678c340c4684fab1ab1309f7e3c48b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c958b1e94844fe82bd76237e6abf81960bddba1791152bf72bc3439337a6ca`

```dockerfile
```

-	Layers:
	-	`sha256:eaa85d15e0879360a29ce1b20bcb5e8679f99cf4ac2aaa673a9dd463316ddae5`  
		Last Modified: Tue, 02 Sep 2025 03:25:24 GMT  
		Size: 3.2 MB (3164781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a9310a5c301b0f3fed84663782a9ef9fa56bd87cd9df420df5dd04804bdce37`  
		Last Modified: Tue, 02 Sep 2025 03:25:25 GMT  
		Size: 38.4 KB (38395 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:70421d1f2927c33550f8084cf229d2865c4af9c37d21746d5c081575205c8eb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.2 MB (521163611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974a94913da3ca38fed95d51cc5c259993b871a5064698341dfafeb48521b28f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0455cea492cc536bcbe5f171a4b7bfd5e6e5ea914fcbf6c745b633f850d31e5`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 4.5 MB (4498593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210f4609a81fb730494c0f54e0ee292e756452bd72736b5a9ca1a40c1d1f6937`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f8984123e1cd60065747b170751561d80e138808b18ec5e371b88c6f70808c`  
		Last Modified: Tue, 02 Sep 2025 02:16:22 GMT  
		Size: 487.5 MB (487514092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc63e79d45924beba020d9a355c9d1587cf695c8f14542cc7a141f2e1027dc4`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293aca7c940831e4255629d203b880bd6a684bc8a8ef8a562ee0cd046a051a20`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718a090f0c5a90eccfcfea8a5fdfda47fe81f82e7f4c7d9388864e83566a0d6d`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 160.4 KB (160365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5eec739e8c569c15257a1cf88310b8687625d5d0844ecff3aa3ed39e13a617`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09b921161b9824c083a45372d4108e9db05de775eb08a76035590d4eb63735a`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 115.5 KB (115542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:16c5ebe0f3cbb9170cb5463bc0409dc27a6a381b602847f8120a1a719066ca3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956050138afc35b10db93f97dd7fac06f529796a4a6b3b7c190a964ef6b93b66`

```dockerfile
```

-	Layers:
	-	`sha256:33dea574cb2cb62888eb7ef77c3947f49dddc003920800e28d440ffaa760e971`  
		Last Modified: Tue, 02 Sep 2025 03:25:31 GMT  
		Size: 3.2 MB (3164565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a854b9a86b5b7f68181341782aaab6ad0e87824838a11fabfe8e368e77f295d`  
		Last Modified: Tue, 02 Sep 2025 03:25:32 GMT  
		Size: 38.6 KB (38599 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.18.5`

```console
$ docker pull elasticsearch@sha256:efbd3a49f62936c21d89e24cbc33ea60f7ee988431d256fdcc82f3eef4093595
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:8c1a65ec85b671ffcc46f582cd3fab211acb49b20e3cd2374bf606967c5f0cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.2 MB (688196464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d70e7d6eae36975e3215d807c736ed243e09caa97e356ec405d056f30b2db7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:34 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:42:34 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.build-date=2025-08-06T22:11:13.597825044Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1fe650052fafd984ded08146c77c6b71b7da7dec org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.5 org.opencontainers.image.created=2025-08-06T22:11:13.597825044Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1fe650052fafd984ded08146c77c6b71b7da7dec org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.5
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89573d801d3ba84aa6fac1fe705124d4424c2b636a247a42682caea8e31c9474`  
		Last Modified: Tue, 02 Sep 2025 00:25:40 GMT  
		Size: 4.5 MB (4493726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228af92b74d71edc7ece011ec41487a90a44af8ad9ac64746605d39ca9f17e0b`  
		Last Modified: Tue, 02 Sep 2025 00:25:40 GMT  
		Size: 3.5 KB (3531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561556f2e0da082b252e3608bec5b77dc2f468a06ebe7044725a17fac9df743a`  
		Last Modified: Tue, 02 Sep 2025 03:48:53 GMT  
		Size: 653.7 MB (653684984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650603c4467547fab87aa26ccf5f36c8cde54a13f8e6c31944bd612807f95cd9`  
		Last Modified: Tue, 02 Sep 2025 00:25:40 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011e47c00ddb4602ce83086e1ab869a056d8627b9bf5da1c5d910ca822f24a19`  
		Last Modified: Tue, 02 Sep 2025 00:25:41 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d964772406723ba0d736e028dc6c090eb3fda2ba4e5b11216794f96b8f569e8`  
		Last Modified: Tue, 02 Sep 2025 00:25:42 GMT  
		Size: 163.9 KB (163936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f4f972f8b63e84b86d02f09fa75d8e649cdfdd3fccdcb52364a87653f6daf6`  
		Last Modified: Tue, 02 Sep 2025 00:25:42 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27506900f9ba9c3fbd81e0d6b0e164cb6f179983316cfc18020b8c1edde21c6`  
		Last Modified: Tue, 02 Sep 2025 00:25:42 GMT  
		Size: 115.5 KB (115536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f59752638a8267b7c6f457705db028cc69f9b75da8817312c533e6be9129bf7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3235875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301445008e8e6ac644bee33514b94769dd63e2e87440086983c4a6771bb2418d`

```dockerfile
```

-	Layers:
	-	`sha256:7c7c6efd63458714528608443800a491480d1d8949b1141a3ac29adfb07be95a`  
		Last Modified: Tue, 02 Sep 2025 03:25:31 GMT  
		Size: 3.2 MB (3197486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e726aab47697a6de3af909be13e3672892772607347b19ecffb8d295ff791e29`  
		Last Modified: Tue, 02 Sep 2025 03:25:32 GMT  
		Size: 38.4 KB (38389 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:5c60fe7d72a335e6e56c724c440b55d022a4adfff568838fec5bba6ba8d36d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.6 MB (530577691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd1310eaca546853250681d12130b9416793d2e4db0d102db046ab11ae66826`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:34 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:42:34 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.build-date=2025-08-06T22:11:13.597825044Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1fe650052fafd984ded08146c77c6b71b7da7dec org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.5 org.opencontainers.image.created=2025-08-06T22:11:13.597825044Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1fe650052fafd984ded08146c77c6b71b7da7dec org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.5
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0455cea492cc536bcbe5f171a4b7bfd5e6e5ea914fcbf6c745b633f850d31e5`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 4.5 MB (4498593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210f4609a81fb730494c0f54e0ee292e756452bd72736b5a9ca1a40c1d1f6937`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c646cb1a2fa0d73928aae355b5411175b37db21c482ea55411b5ad76175099f`  
		Last Modified: Tue, 02 Sep 2025 03:26:08 GMT  
		Size: 496.9 MB (496928155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32eed46ff09699f7b044d28de53a9031ff37bdaccac3587c86794123350b3b5`  
		Last Modified: Tue, 02 Sep 2025 01:13:02 GMT  
		Size: 9.1 KB (9107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4e8726565d79225ce7611196cebf1e3757f29220cf4ad60510150755ef7642`  
		Last Modified: Tue, 02 Sep 2025 01:13:03 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c6067cea85025f19589ebb950a64a6ed2a22430f4426fda71419079c5f2707`  
		Last Modified: Tue, 02 Sep 2025 01:13:04 GMT  
		Size: 160.4 KB (160375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e453c644e24650776f274996ed290d644b016ca8f8495073570a9cf2bc0c523d`  
		Last Modified: Tue, 02 Sep 2025 01:13:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac497796c28ba0f64f4e4350bfcdc49be8453882a8e496045d2e0c35c33116a1`  
		Last Modified: Tue, 02 Sep 2025 01:13:04 GMT  
		Size: 115.5 KB (115540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f05a6ce70116cfe4c4cc81f6b592f7b7e1c19e4223fb15f44607474ccf7fc70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3236491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870db2907e7beb949fe8da7c460507571bd269d4da6b88596eec95753f08009a`

```dockerfile
```

-	Layers:
	-	`sha256:5bb819f18fe9bef1291a8c96d3e9ca884b6fa60a027cdcc4c2a126c7c4d267cf`  
		Last Modified: Tue, 02 Sep 2025 03:25:36 GMT  
		Size: 3.2 MB (3197899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2e99e018b7d995fa22819bce246abd3948a1c3444002a257b30bb5334d6fc1`  
		Last Modified: Tue, 02 Sep 2025 03:25:37 GMT  
		Size: 38.6 KB (38592 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.19.2`

```console
$ docker pull elasticsearch@sha256:a083dd01d191f2aad411953eb8d02d3bb2938c6fe98ef3164919ff3cadfe0786
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:fcda0e8d5e03acecc1207e3630ec2bbb46f73fe6ab6c763345becfa339169926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.9 MB (694945794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cc4c6c88071f41054571da7524353e12be7b386c5fb676482f0d92fa226d8c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 11:48:35 GMT
ARG RELEASE
# Tue, 12 Aug 2025 11:48:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 11:48:35 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.build-date=2025-08-11T10:07:54.721189302Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1c00e18ef14acd650768ff01f037eaede0c1f7b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.2 org.opencontainers.image.created=2025-08-11T10:07:54.721189302Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1c00e18ef14acd650768ff01f037eaede0c1f7b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.2
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3596f07655306bc29a36fff42203c68c433743e8128957e892b4e948e2c122`  
		Last Modified: Mon, 01 Sep 2025 23:10:01 GMT  
		Size: 4.5 MB (4493659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfad3f9bdc77b516604c47fd36c7b3d5001e5e6f7912a21640f604bdbc34e1a9`  
		Last Modified: Mon, 01 Sep 2025 23:10:00 GMT  
		Size: 3.5 KB (3530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7622a10faf19fd7d3db7670ac882b4f65ea82721818679cfa7f0b6cae6e9b21b`  
		Last Modified: Tue, 02 Sep 2025 03:26:30 GMT  
		Size: 660.4 MB (660434365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0ac3218cc53a58d63ec6027bef6b7cc06fc5701e82f70443fafb603a2fdcbe`  
		Last Modified: Mon, 01 Sep 2025 23:10:00 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb5cca9dbd92be7e04702cf03e2abdfd34ed57e9454fd30cdadb5df5852d7b3`  
		Last Modified: Mon, 01 Sep 2025 23:10:00 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb288cdce1ee9fd45d90f960752126f34ca10cf81a16cae24fa931d8ff4bf6d3`  
		Last Modified: Mon, 01 Sep 2025 23:10:00 GMT  
		Size: 163.9 KB (163945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8b065ea512733d57949e494977e270100ada220fb582cb7806f88327f29d24`  
		Last Modified: Mon, 01 Sep 2025 23:10:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf5e6aed117c437956ab1e07ef7e6c12de3b5d86da45fb36448e654abdad3d8`  
		Last Modified: Mon, 01 Sep 2025 23:10:01 GMT  
		Size: 115.5 KB (115543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:12832cc167aaece4ad2ada919c226848df9ef5d9e6e98c45477a6be4c779e147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3255286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea382e070e9a4bc34297562ee8c00a1190a8e5c38ab96a53c09c2a409feb1b15`

```dockerfile
```

-	Layers:
	-	`sha256:0c886e44a573c3a7e08bb22931cd721df9461852ee6425c5bf2cbf9781bf39c2`  
		Last Modified: Tue, 02 Sep 2025 03:25:41 GMT  
		Size: 3.2 MB (3218403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e079e261da824d36b67c8a324a50c80dcea422b48004d806d71ebafa8bcc7ea7`  
		Last Modified: Tue, 02 Sep 2025 03:25:42 GMT  
		Size: 36.9 KB (36883 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d4c716563cae8319c4452c7b6fcb1da01e3276be7fa12e8544f1e12da11f1368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.3 MB (537319826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7c8dabba46df9b0266f5a1d59ab670d3a6dca8ca2e3abf9afdd161204dde0a`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 11:48:35 GMT
ARG RELEASE
# Tue, 12 Aug 2025 11:48:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 11:48:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.build-date=2025-08-11T10:07:54.721189302Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1c00e18ef14acd650768ff01f037eaede0c1f7b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.2 org.opencontainers.image.created=2025-08-11T10:07:54.721189302Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1c00e18ef14acd650768ff01f037eaede0c1f7b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.2
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f16f5301b8771135a56997cb07b9dfd4f910447ab2311e639457a0c697c4cab`  
		Last Modified: Tue, 02 Sep 2025 01:15:00 GMT  
		Size: 4.5 MB (4498579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d2ccf21c2e0288fcfc3e1a3dc3f0ccf72fceaa0992eff983d88cebfd5e5eff`  
		Last Modified: Tue, 02 Sep 2025 01:14:59 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f357a32f71362e05cc736117dddec73c3b398f1c4f1de4c33c1aaed60d5c0bb`  
		Last Modified: Tue, 02 Sep 2025 03:27:22 GMT  
		Size: 503.7 MB (503670317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e211ac525b84b18fd512053d1f729fa98253543b155db1822fa73c73fd8293`  
		Last Modified: Tue, 02 Sep 2025 01:14:59 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c93a9effda4f27703511c1b7610eba59aba1504860128864330493959c1532`  
		Last Modified: Tue, 02 Sep 2025 01:14:59 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62aef7a2bd49654e93111e70813289103efc25dfcea5d9eadb4ae6bd0e32e68`  
		Last Modified: Tue, 02 Sep 2025 01:15:00 GMT  
		Size: 160.4 KB (160366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13875c487bac575b4eb6798826cd51e6d2d31e408d0f0cfc0a769485a35b7bb0`  
		Last Modified: Tue, 02 Sep 2025 01:15:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc21a156093984273ac28adc051522698ba69f266a1a41fe5200ce76ded0927f`  
		Last Modified: Tue, 02 Sep 2025 01:15:00 GMT  
		Size: 115.5 KB (115543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8e3e12ee3bf314e8bb76f6d7f4f6081bda472dcecc6d21811a24580e36885c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3255902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d71a374cd62866b9769d88030563db06590d10e01e62b88df6fd791bd9f9ca`

```dockerfile
```

-	Layers:
	-	`sha256:4f4af1f2f1bfdeb744bab3cbf5fa0b155ec1c2ad995bb610304edac5262eee4c`  
		Last Modified: Tue, 02 Sep 2025 03:25:47 GMT  
		Size: 3.2 MB (3218816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e1c53e9d92fbbfc82816ec9a44875cb0f3987e6b8c4b557c89355290d7ad0d`  
		Last Modified: Tue, 02 Sep 2025 03:25:48 GMT  
		Size: 37.1 KB (37086 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.0.5`

```console
$ docker pull elasticsearch@sha256:95f29cf63b861a54c91ec7b1501221353ea95fb0e255acad9b56d8ae3bd2e413
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:edc2551ab68e4b57e4f1669303b32706bd38f992f6c138510090e09b4f7070c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.2 MB (700243672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba689ac832510db777126a2f3d5152c5151a82dc1c2395a28152b764b6fc5b8e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 08:42:57 GMT
ENV container oci
# Tue, 12 Aug 2025 08:42:57 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T22:11:00.741626477Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=abacf6d19441c06668da7264241312caee03cef5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T22:11:00.741626477Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=abacf6d19441c06668da7264241312caee03cef5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.5 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 Aug 2025 08:42:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67bc67af4761ee3bef6b76073d25c0019df4061e1958c6f12d83e8785df3c8b`  
		Last Modified: Thu, 21 Aug 2025 18:57:51 GMT  
		Size: 4.3 MB (4284051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a0710cc067d2af9756405b0a840213bd20aca08b778d314408845c43e67fac`  
		Last Modified: Thu, 21 Aug 2025 18:57:45 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8503dad9e5dd918ec7a70a64a1edf7fff06e88b9e22f26cb3d09c7557c43a92`  
		Last Modified: Thu, 21 Aug 2025 18:57:44 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b5989f2004e5b145f418143623461c76df984491436a51620f38c8957549b7`  
		Last Modified: Thu, 21 Aug 2025 23:29:26 GMT  
		Size: 656.2 MB (656221797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d7b7eed886da1c5b6fb214980a003a07fc741dd3878a3f4b79e18b39c3abd`  
		Last Modified: Thu, 21 Aug 2025 18:57:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94fa7dc01b095811025735df6f82cdb0265c329facce78591d244e9498af7b1`  
		Last Modified: Thu, 21 Aug 2025 18:57:44 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c0e4ee300fb45a4583ee69d8b833611ad05c7b1320bc4be4f3d8c74b4d486c`  
		Last Modified: Thu, 21 Aug 2025 18:57:44 GMT  
		Size: 75.7 KB (75747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357e5cfd9c0a65bed4e7ba9a3860aa096161b1cfde4e3c80cba3c7c1d4fe9cee`  
		Last Modified: Thu, 21 Aug 2025 18:57:45 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c38fb6a579d4bd2cf5aef74b136c54306f43bfd010c87074245fc418e7ab95ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2067638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d826d838ab66901aef114b8657eeff7369bd7bdad6335a62973ea7d87112509e`

```dockerfile
```

-	Layers:
	-	`sha256:c867cf06adc5ceb2755f3408a1e7d38e46a74e449195c0dea2e33015b671d119`  
		Last Modified: Thu, 21 Aug 2025 21:25:22 GMT  
		Size: 2.0 MB (2033799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f52b71269e28ebc11240cb3c86281f2411081cf0d12ff36860fa82ad6646c95`  
		Last Modified: Thu, 21 Aug 2025 21:25:23 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:b6f493b714c0f747e094d16677a9e8e111f878852c768f3ff61a9692c7c49c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.7 MB (538707720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2b92bf2f86fed3fe1be1e9d192530847e2eab57eea8b217e1e23505b10b780`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 08:42:57 GMT
ENV container oci
# Tue, 12 Aug 2025 08:42:57 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T22:11:00.741626477Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=abacf6d19441c06668da7264241312caee03cef5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T22:11:00.741626477Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=abacf6d19441c06668da7264241312caee03cef5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.5 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 Aug 2025 08:42:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8819904c4bbdeaf16699d8b133f573cba66f156c19ee525116de9edb1706d4b9`  
		Last Modified: Thu, 21 Aug 2025 19:11:02 GMT  
		Size: 4.3 MB (4293045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a556c8b5e19f7fe7f0901b590e0d2221f62670c53ab502e0dcde8885393c6153`  
		Last Modified: Thu, 21 Aug 2025 19:11:00 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f95e25f6efd13f00804818183cf4256e19126ec91f6531ecc13bf4c7729264`  
		Last Modified: Thu, 21 Aug 2025 19:11:01 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255bafcb0367af1a2542f155d565fc17b3479609e45566af503007aee8dbf935`  
		Last Modified: Fri, 22 Aug 2025 05:53:16 GMT  
		Size: 496.5 MB (496466096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23afe729ba6234320b894ac11814ad7441cab3c2b2e4c3c6223a8644c3df723`  
		Last Modified: Thu, 21 Aug 2025 19:11:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad02e23492309edf8c6c3bb28154add8aa4af3cf42530885c677bb22cd3c6c71`  
		Last Modified: Thu, 21 Aug 2025 19:11:01 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9352a77d41c2ab8119bc267df715d9a7935cdd1f6a70c837dfc5a8632b364444`  
		Last Modified: Thu, 21 Aug 2025 19:11:01 GMT  
		Size: 74.6 KB (74644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870bcad31b1d2441179324c043dde4ff97d89af8c2c045589de71ec4c9211720`  
		Last Modified: Thu, 21 Aug 2025 19:11:01 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e3ca8df0277b3244fadf279c10fa24471eebda4c4737a32f351e4ae487a86cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8a21f0b9a3dd5fdaf4984fdc9915819245a514d28410039b417fe253e81f63`

```dockerfile
```

-	Layers:
	-	`sha256:c417e8e69f68f935392f3b88b0c86ca7701ec7b098f5d8bd12f815f8e976523e`  
		Last Modified: Thu, 21 Aug 2025 21:25:28 GMT  
		Size: 2.0 MB (2034363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a565841354900a57ef557b8b2a37133c32c59379348b9ed3408fcb0c2a3563`  
		Last Modified: Thu, 21 Aug 2025 21:25:29 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.2`

```console
$ docker pull elasticsearch@sha256:59ab37a27e457c0e801a0ce9c1233ba47b81f0d907d3dbf8a413f620e411eb83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:d7e6cf7cae9b356cef2ca22d1a19696fd7d2ca7035e2689e3e38d784ce2dd61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.3 MB (715263897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0370c61f362b88a0a67d030f1c85970eb435bccd251cc5f70bfbcc7c15d50dbc`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 11:49:08 GMT
ENV container oci
# Tue, 12 Aug 2025 11:49:08 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-11T15:04:41.449624592Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=ca1a70216fbdefbef3c65b1dff04903ea5964ef5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-11T15:04:41.449624592Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=ca1a70216fbdefbef3c65b1dff04903ea5964ef5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.2 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 Aug 2025 11:49:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa33d5017b50c8b81f51ad7e4b89f05191c17c1060cdb2cdf195b1748b5f4f`  
		Last Modified: Thu, 21 Aug 2025 19:11:40 GMT  
		Size: 4.3 MB (4284011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ad447871662cffcb23f6602e68e378bcfe48bf86658ac1e0544574c69c3b14`  
		Last Modified: Thu, 21 Aug 2025 19:11:40 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802114e09db323d502aee10a5eaeb9764c4e875bddd64937bc94a33c6075ed99`  
		Last Modified: Thu, 21 Aug 2025 19:11:39 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f729a66d74063eafda896c7a70166018059b370c25c94b0e0a6a2e02ecd83c6`  
		Last Modified: Thu, 21 Aug 2025 21:26:21 GMT  
		Size: 671.2 MB (671242059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e755dec823cc88c5f876e3c1cb188a490d8d27b0540718a659cb138531e652cc`  
		Last Modified: Thu, 21 Aug 2025 19:11:41 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd9405f5c2999ee71893d3d9d5bc4e4b3ab697dc40d4542203954175eaccd3`  
		Last Modified: Thu, 21 Aug 2025 19:11:40 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22568f2f520f49e439cf2129403897bcb05fc93c018a522e34aae147b0ae53b0`  
		Last Modified: Thu, 21 Aug 2025 19:11:40 GMT  
		Size: 75.8 KB (75750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e01424e0dcb6270c9c3177748afc008ebabc6929a2102222d04003805c13d0`  
		Last Modified: Thu, 21 Aug 2025 19:11:41 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9a4aab714437e9ecbabc9c83ac5e8bbb7193a45bb17c434eaa5017b4d954b2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3138af6c8f14c3de127b07e514da75cec06a4e17b7dae7d3d82c12adfae8e0`

```dockerfile
```

-	Layers:
	-	`sha256:b8c5c8d0a00d9ca19726292f24512a33cc932be9979bc72176a27da0e946a693`  
		Last Modified: Thu, 21 Aug 2025 21:25:31 GMT  
		Size: 2.1 MB (2088158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d65aa61808b3ddf3d01c52b71e79d1122cba66f8747bf2f84096b9fa0fc376`  
		Last Modified: Thu, 21 Aug 2025 21:25:32 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:2b858546f971448bcf3bd35326de4633c6656bad86d322041c257c25f13f31ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 MB (553730527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f96ee554191ed5fb0239354ee5111416750a1dbb40c7535673c9c8da5089d`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 11:49:08 GMT
ENV container oci
# Tue, 12 Aug 2025 11:49:08 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-11T15:04:41.449624592Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=ca1a70216fbdefbef3c65b1dff04903ea5964ef5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-11T15:04:41.449624592Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=ca1a70216fbdefbef3c65b1dff04903ea5964ef5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.2 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 Aug 2025 11:49:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8819904c4bbdeaf16699d8b133f573cba66f156c19ee525116de9edb1706d4b9`  
		Last Modified: Thu, 21 Aug 2025 19:11:02 GMT  
		Size: 4.3 MB (4293045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a556c8b5e19f7fe7f0901b590e0d2221f62670c53ab502e0dcde8885393c6153`  
		Last Modified: Thu, 21 Aug 2025 19:11:00 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f95e25f6efd13f00804818183cf4256e19126ec91f6531ecc13bf4c7729264`  
		Last Modified: Thu, 21 Aug 2025 19:11:01 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd77c4456ef874d16943397fd85331d7dfc4f13a92c6cfbd18cd9b50851d36ff`  
		Last Modified: Thu, 21 Aug 2025 22:10:29 GMT  
		Size: 511.5 MB (511488900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a507638ab0d3a20f24db9c8a9b6e1ad5077c16cea1acb3f1f8f3c4837a05cf`  
		Last Modified: Thu, 21 Aug 2025 19:13:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd92fbd82d25ec7e922d13525c24fc3a66edd3ece1591e6512e56443ef52a0d5`  
		Last Modified: Thu, 21 Aug 2025 19:13:04 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f2a5180b68254a3d6533587cdfd0ec0c408fbefeaac7fca29acaef2d8b2569`  
		Last Modified: Thu, 21 Aug 2025 19:13:04 GMT  
		Size: 74.6 KB (74648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7ce74ae9e83a62d8d8e31091d028f354e244e311e6ed7d594504dd8331e4af`  
		Last Modified: Thu, 21 Aug 2025 19:13:04 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:cc23e77b7c492b9d5062645f1fd137db19491239cd8bfbc6192c17a79f9f5e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0b95ad11435a70eadc7e940afb285aa696fb333cc31e59385a82569d14803a`

```dockerfile
```

-	Layers:
	-	`sha256:db9869c6e1e12a30ba341817209857da80602278a583c0c9ca8276484372daa3`  
		Last Modified: Thu, 21 Aug 2025 21:25:37 GMT  
		Size: 2.1 MB (2088722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91bb809be470c698d842825f6acfa5c2eb26b2c219925692f07a2f581f1cd20f`  
		Last Modified: Thu, 21 Aug 2025 21:25:38 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json
