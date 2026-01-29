## `openjdk:27-ea-6-jdk`

```console
$ docker pull openjdk@sha256:8bf29cb4ee7b68756edf372dcdea4f1ed70eeff83d3171f1051e6091eec4eb77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-6-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:67e90d5266967d794e7763a14ae6a2af375fceaec0da629d476b74980e5b2e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313834235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8854bf0e351b4ebdb7765691d252648d55a98a746c51b893667f85e400b8af0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:12:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:12:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Wed, 28 Jan 2026 22:12:36 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 22:12:36 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 22:12:36 GMT
ENV JAVA_VERSION=27-ea+6
# Wed, 28 Jan 2026 22:12:36 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 28 Jan 2026 22:12:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5d45c47ad951c2691e62302c3f12e58bad39e8efb583c72058c42d774cc7c`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 38.3 MB (38296127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0caebd8be029d3d5bb1c78c32031d7aae3a6f64a5329ee5e5e6847362dc27c2`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 228.2 MB (228225394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-6-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:e5666e848a97816ab4dee78b6880c60cff4ac90c3d395b994ac45863427c68f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e76a7fe0c44fa111c88c0660b8efc005fa88283fed41918787835ca95a98045`

```dockerfile
```

-	Layers:
	-	`sha256:5d5c29f3edcf363dcd6f7cddbef5a5b6799ecb7e8fe5c952b6d9ea9b6e6227a6`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 3.7 MB (3655375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0455f3b65a4c2aba8b62ee51ce3058b02156af3991d1e8c6b8532137764e32cb`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-6-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dce842829244f19760c4cd9c8fab7c9b989c2aa7c57b8614c97b781ee5a4735c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310744085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e937b8556f61c55dfb0b83cccd7e15b6af37ae3abf7e375218bddb56fbaa1114`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:12:02 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:12:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Wed, 28 Jan 2026 22:12:12 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 22:12:12 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 22:12:12 GMT
ENV JAVA_VERSION=27-ea+6
# Wed, 28 Jan 2026 22:12:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 28 Jan 2026 22:12:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289423e4c58521d9c4ebdb604f7edc16a15b0eec01c87b7bc5d19ddbaab90e18`  
		Last Modified: Wed, 28 Jan 2026 22:12:35 GMT  
		Size: 38.7 MB (38692413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d9de4ec420a20c679fcc9c81d3b8b39fe00352c1da4775cdc24ee05100c478`  
		Last Modified: Wed, 28 Jan 2026 22:12:39 GMT  
		Size: 226.1 MB (226148444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-6-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:ecda646ad3c40d2f27d46984896af7c3b58b8b1af49faf63c352f72ae79d2aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f5c0bd5ffcd130090e5d56e255e4269578a2d321ad7c2c6c883e9725f3c523`

```dockerfile
```

-	Layers:
	-	`sha256:8f3468a1c6609ec26586023ecc455a2487dba4b9df83314d76ea68481abf836e`  
		Last Modified: Wed, 28 Jan 2026 22:12:34 GMT  
		Size: 3.7 MB (3653065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61521e6555b3b03044ec0bf88db9f24c70de643327d88021d841e535adbd4160`  
		Last Modified: Wed, 28 Jan 2026 22:12:33 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-6-jdk` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:7d859c1b2378ad3253e2b654a7bd6f707fa8ec73eb2fa6c969addfba8c19ee26
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1721185849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651f5f69ec50448acefcd6ebe54218772bd068d9e11033f300e9fee07cda4e39`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:08:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:34 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 26 Jan 2026 22:08:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:39 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:08:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_windows-x64_bin.zip
# Mon, 26 Jan 2026 22:08:41 GMT
ENV JAVA_SHA256=dad15ea855765f796d0a975373f5f6aa7e247d717d129641177c41ee0cbe211c
# Mon, 26 Jan 2026 22:09:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:09:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a1ee0bf0167df6115953b6b1b098fa7a7d283b273426e6102f22f9f9cda0ab`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 403.9 KB (403850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48792ea1b7025d5b1254b2044b585783cbec73f35e438ff315edd7d77db07472`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c729d92fcc29b96e35583ec02da675ce9c8fb502e913f8fec07ceb5600d74a`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 388.8 KB (388796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442a4e75aa3f26e3e8f67ca78b91e4f42f950497956d9d357722aa918051f139`  
		Last Modified: Mon, 26 Jan 2026 22:09:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af94527c78e3478cc47da34e9d0a8333a10af87043c6239e5a3c6c519e3e8116`  
		Last Modified: Mon, 26 Jan 2026 22:09:20 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c936ac13317978a6f488e1712e5c16379ebaae55ef169b5015d4cc0a207c0a`  
		Last Modified: Mon, 26 Jan 2026 22:09:20 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40d0fbb771a150b90d600acb5d48bc7182a335e1011814b69ebe9d6d3c1e882`  
		Last Modified: Mon, 26 Jan 2026 22:09:36 GMT  
		Size: 224.6 MB (224625010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609f3fe84f8db0453942811ffc4bca8a6c16f9244eaddb4132c8cdace10323f9`  
		Last Modified: Mon, 26 Jan 2026 22:09:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-6-jdk` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:f1c30f1c79ce04119ee0f5888fa67eb14e937ca497455edae64f56b283661564
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2061109356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b8415637416d3e715dbd56186c0e96cb9ab50c9038f9c40ee34c45f9e3878`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:08:48 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:49 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 26 Jan 2026 22:08:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:57 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:08:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_windows-x64_bin.zip
# Mon, 26 Jan 2026 22:08:59 GMT
ENV JAVA_SHA256=dad15ea855765f796d0a975373f5f6aa7e247d717d129641177c41ee0cbe211c
# Mon, 26 Jan 2026 22:10:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:10:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76ff2a09c21b3d7e083854bf410cec2dd68e42740043ac4fdacd0bc8265ef2a`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7334237da746dd9e131c778b3600cb33732f93a96573dc62e7380e5750fd3306`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 503.6 KB (503582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42fb1fae328f7f30004d4efada45f6777936c5d10b6a930d2c3ef352702a331`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec55cedc65038f0cdb1737c1058132c56ccd231620d1285ece72d3d6e91f2228`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 351.9 KB (351912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7dea516e5f8ca3463a39f472c44a87df6eb8aace60d4cb821e963411f9669b`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7465b25cd00fe3671ce1b3b27c1bbe25f74fbc623a463ade80b41568f4ea1aee`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d20f5d994a0533e7e95525f64fd6104318d4a7203e7d0399b315f433ca2354`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60649b02a4261f297ae8ff3516a51c6abc875019bc452e5e29f28023f973d2e`  
		Last Modified: Mon, 26 Jan 2026 22:10:41 GMT  
		Size: 224.6 MB (224586810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4797cbc191a1fe112d4ab6c47be1f2696475a364491bb0240c48d5049e6dc72`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
