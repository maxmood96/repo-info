## `kong:centos`

```console
$ docker pull kong@sha256:571c7f5baa933668359aad9802ef048fb0c522b782333248fa2f5e07595f9d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:d241c5143fff7f234c6b2b56980979e69b6a02a8acdd4c96a4edf70a3c6688dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158228534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7078e29bd7b317f71822cded25a54899216da7ab71126a3492314f6cba57f25a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:32:03 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Wed, 05 Feb 2020 23:32:40 GMT
ENV KONG_VERSION=2.0.1
# Wed, 05 Feb 2020 23:32:45 GMT
RUN yum install -y -q unzip 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki
# Mon, 10 Feb 2020 23:24:49 GMT
RUN useradd kong 	&& mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chmod -R g=u /usr/local/kong 	&& yum install -y https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm 	&& yum clean all
# Mon, 10 Feb 2020 23:24:49 GMT
USER kong
# Mon, 10 Feb 2020 23:24:49 GMT
COPY file:4c514f433339e8232479c5f83c4abe18fa083902b64cf695d83937fc4947437c in /docker-entrypoint.sh 
# Mon, 10 Feb 2020 23:24:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 10 Feb 2020 23:24:50 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 10 Feb 2020 23:24:50 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Feb 2020 23:24:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0519344698532b61d589f23f1f1283696c4aea5a0bc98f0723c5804873560`  
		Last Modified: Wed, 05 Feb 2020 23:35:01 GMT  
		Size: 6.6 MB (6569287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f829582a1bcfcff29fd617e62f3b45de4821e42649777d8323c27500a82be6b`  
		Last Modified: Mon, 10 Feb 2020 23:27:29 GMT  
		Size: 75.9 MB (75878180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905d795beaef376eabf9019dbfd316fae1c2c7ec3b6793aa72ab12125f6442e6`  
		Last Modified: Mon, 10 Feb 2020 23:26:30 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
