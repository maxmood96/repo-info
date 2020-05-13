<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:6.8.9`](#logstash689)
-	[`logstash:7.7.0`](#logstash770)

## `logstash:6.8.9`

```console
$ docker pull logstash@sha256:779bb4dee77b7d960b44fb21a794a92a9603612d036b7e40aa5ad15930480bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:6.8.9` - linux; amd64

```console
$ docker pull logstash@sha256:b92c1c35e61b490fa36e5240ddd74a940d2615a1f7d2ee47e79fdad18de731fd
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.1 MB (393110456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7ba45ec284e4e93ba0834f7a1b40322acd0934247bdcc5212a22f872c79372`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2020 18:38:26 GMT
RUN yum update -y && yum install -y java-1.8.0-openjdk-devel which &&     yum clean all
# Mon, 04 May 2020 18:38:28 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Mon, 04 May 2020 18:38:44 GMT
RUN curl -Lo - http://localhost:8000/logstash-6.8.9.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-6.8.9 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Mon, 04 May 2020 18:38:45 GMT
WORKDIR /usr/share/logstash
# Mon, 04 May 2020 18:38:45 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 04 May 2020 18:38:46 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2020 18:38:47 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Mon, 04 May 2020 18:38:47 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Mon, 04 May 2020 18:38:48 GMT
ADD file:2ef21d4766eab3ac48ed3847c8b8d05554f1fd0b39061cba66c9ac93240087fa in config/ 
# Mon, 04 May 2020 18:38:49 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Mon, 04 May 2020 18:38:52 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Mon, 04 May 2020 18:38:53 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 04 May 2020 18:38:54 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Mon, 04 May 2020 18:38:55 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Mon, 04 May 2020 18:38:55 GMT
USER 1000
# Mon, 04 May 2020 18:38:56 GMT
ADD file:cebf0ff7ebe120c237a4cd02789b4d90543b551aaeb6a2e695b7ed3070e28792 in /usr/local/bin/ 
# Mon, 04 May 2020 18:38:56 GMT
EXPOSE 5044 9600
# Mon, 04 May 2020 18:38:56 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=6.8.9 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Mon, 04 May 2020 18:38:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5133995aa978dd2530f0f34f840c60a8c367b53b4297eae4cf247831675703e9`  
		Last Modified: Wed, 13 May 2020 16:19:47 GMT  
		Size: 135.7 MB (135681179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb58783d269788ef44e0b9c1a8d9e66890674e20994e7a35b35b0185d13c9244`  
		Last Modified: Wed, 13 May 2020 16:19:21 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca07f40498fb9e6938f692ca0fea767391fe4a8f7ba411e56a5795c46d39e35c`  
		Last Modified: Wed, 13 May 2020 16:21:31 GMT  
		Size: 180.6 MB (180637275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5728f2706788bce038797d7b199735ef5d8aee95845ba88fc89bd3bf42d8fcc8`  
		Last Modified: Wed, 13 May 2020 16:19:21 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0baf9f1afb8fdb3c88a5fc3830b2f535f888ff6ff58beb005f30d8f546818141`  
		Last Modified: Wed, 13 May 2020 16:19:21 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2607e87ac29e512225043587f1da02cd1b4ee5fe4d1c4ad6fad9545d8b2aab`  
		Last Modified: Wed, 13 May 2020 16:19:19 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa32d0fd671b445110147d19e28ea6e9d20fc773fc2726909c02d33109f4ba7a`  
		Last Modified: Wed, 13 May 2020 16:19:19 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c1e4fbd878e3fca2e6a9fe33b7361a892ed3203dbe0c1b36ea6d0efb0e8797`  
		Last Modified: Wed, 13 May 2020 16:19:19 GMT  
		Size: 2.7 KB (2678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a745219cbcfab4839c540815081b18d1e77f2a0f46c709a4aa12b38a129c7fb`  
		Last Modified: Wed, 13 May 2020 16:19:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a745219cbcfab4839c540815081b18d1e77f2a0f46c709a4aa12b38a129c7fb`  
		Last Modified: Wed, 13 May 2020 16:19:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1630decb87beaaa51adf53c604c65505f37e29daa1de6c3aae8e16ee4e9a3c`  
		Last Modified: Wed, 13 May 2020 16:19:19 GMT  
		Size: 1.0 MB (1004413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `logstash:7.7.0`

```console
$ docker pull logstash@sha256:8a3665c521e7b6b1517bb1fad320e2db87f93e2c6f098dd04c7e119a3c0d2017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:7.7.0` - linux; amd64

```console
$ docker pull logstash@sha256:a773e631967f0b99893f636d08f4724914d39bb78b14e8025ceff394f278f8f4
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325844827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dcca1db5e9ba1429b3ae0eba003e726281f733f4f5845ddc2c2a84fb78e8db`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2020 04:44:16 GMT
RUN yum update -y && yum install -y java-11-openjdk-devel which &&     yum clean all
# Tue, 12 May 2020 04:44:17 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000       --home-dir /usr/share/logstash --no-create-home       logstash
# Tue, 12 May 2020 04:44:31 GMT
RUN curl -Lo - http://localhost:8000/logstash-7.7.0.tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.7.0 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash
# Tue, 12 May 2020 04:44:32 GMT
WORKDIR /usr/share/logstash
# Tue, 12 May 2020 04:44:32 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2020 04:44:33 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2020 04:44:33 GMT
ADD file:1183410472ec370104718a08e1144081518db1d006a8cc82de824a34455ab3f3 in config/pipelines.yml 
# Tue, 12 May 2020 04:44:33 GMT
ADD file:83ab096464b764c812ae68c2872c05d48ee1620e6a1629948d52c13ac6dcfe11 in config/logstash.yml 
# Tue, 12 May 2020 04:44:34 GMT
ADD file:4f39d77a8986c28d67e673d4691e69ca9c175574128b0819977c2d1bb0d6e950 in config/ 
# Tue, 12 May 2020 04:44:34 GMT
ADD file:0cd9cc51daf5f37b2aa8aae8cf3570a3680e22852afb2803ccb87ddcd3369f52 in pipeline/logstash.conf 
# Tue, 12 May 2020 04:44:36 GMT
RUN chown --recursive logstash:root config/ pipeline/
# Tue, 12 May 2020 04:44:36 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 May 2020 04:44:38 GMT
ADD file:29dd60f159d64086c20a7a02f84a9314f44b2290304547233fb96744325b1245 in /usr/local/bin/ 
# Tue, 12 May 2020 04:44:39 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint
# Tue, 12 May 2020 04:44:39 GMT
USER 1000
# Tue, 12 May 2020 04:44:40 GMT
ADD file:e85ef9ade5cf1783b35df4b4a436e8083e3b9d902c90bec5cf6a617e5a160a65 in /usr/local/bin/ 
# Tue, 12 May 2020 04:44:40 GMT
EXPOSE 5044 9600
# Tue, 12 May 2020 04:44:40 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=logstash org.label-schema.version=7.7.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash license=Elastic License
# Tue, 12 May 2020 04:44:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676f059574bb01ba41a1a5de2b14f6073f0956d3399ea911aa2af4568872ccea`  
		Last Modified: Wed, 13 May 2020 14:02:41 GMT  
		Size: 81.8 MB (81817427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e974e49ddee748711d9b91dd01ed14ccffcc3c6d8a5cb1bf7e8905ea68986f1f`  
		Last Modified: Wed, 13 May 2020 14:02:18 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3423b075bb4a8327ce4979548a021e04561022438bad1dfa2ba4bf1143f8c94c`  
		Last Modified: Wed, 13 May 2020 14:03:37 GMT  
		Size: 167.1 MB (167135723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01d6bcefef99df29c9df52ad16880803333914280707acdce3d854aa53e8d7d`  
		Last Modified: Wed, 13 May 2020 14:03:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5859d91fec223df2fa122ed6423d08ab8e17d21c7583b861693d88e903fb1330`  
		Last Modified: Wed, 13 May 2020 14:03:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4d032772144dc449ac42fb955a921698bbde3b276391f7a0f368859315d1c6`  
		Last Modified: Wed, 13 May 2020 14:03:17 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f51455693d8a4d264ece3d78a23effb9d8f1cc91471216444707316d2b84d4c`  
		Last Modified: Wed, 13 May 2020 14:03:17 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8474cc37cb136108b316aa4c425f425b172e8676a495c45bc2aabeb8cd01caa3`  
		Last Modified: Wed, 13 May 2020 14:03:17 GMT  
		Size: 2.7 KB (2748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f382646ef97780fc55b0e914da954150bd93e1ac52165553079fd7e24c2c3`  
		Last Modified: Wed, 13 May 2020 14:03:17 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f382646ef97780fc55b0e914da954150bd93e1ac52165553079fd7e24c2c3`  
		Last Modified: Wed, 13 May 2020 14:03:17 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac989b6ae1c97a33a045ba7fc15fe538635429dae6b2a26101a8ba504fbe70a`  
		Last Modified: Wed, 13 May 2020 14:03:17 GMT  
		Size: 1.0 MB (1004563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
