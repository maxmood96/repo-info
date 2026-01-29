## `openjdk:26-ea-32-jdk`

```console
$ docker pull openjdk@sha256:184917c0d5e12bd8578f5a19be18a581e49c76d1fb011ea53235e042dc241bc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-32-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:1bf96b0382269e91123421097e7cb8abdce6cc44fd7b98a17720bb33dc2b9bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313475776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83395350716c1c4c7ecd08dc85283c025d9a32a023f19aa08af2570ea93d53a0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Wed, 28 Jan 2026 22:12:39 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 22:12:39 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 22:12:39 GMT
ENV JAVA_VERSION=26-ea+32
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='99e956807a500a396bc799f5b450e79c295bccece78ae9ca67f3e75646d3a099'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef6d53835db7740daeda9be917698b14f742df288966e4985504f7f2e465ad0b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17e94958ce11086530cb108a2252cc6445e86fb183d565e3d26ec1f5aab7776`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 38.3 MB (38295590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb99fb3196ab850058fe4a698e34f84472f7a9556092ab110d1b95816b086d7`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 227.9 MB (227867472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-32-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:d274f82f25efbeb72ac08b80b33dd456a41b183d981728a3ad29f7b3effa9f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc69af40e19b24630c00ff24fdf3b5568369900120c8ffdb9e739fe5080e5e2`

```dockerfile
```

-	Layers:
	-	`sha256:128a65d6fe6c7da03bb252ea8227a64f4dd93ae33076676fa203496eff73c840`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 3.7 MB (3655391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d69ce2a9d147a37f7ee0bceec1cfc9c6a4b62d8ce4b7f499bcb2efc11db76c84`  
		Last Modified: Wed, 28 Jan 2026 22:13:00 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-32-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2fadc3ab1c6328db30f2a98696f4713c211ca09091a6ce97237b413b731f2c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310380700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9da70668be6defdea3e70d855fb395289d9176dadd20293fb779b95c1255a7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Wed, 28 Jan 2026 22:11:40 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 22:11:40 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 22:11:40 GMT
ENV JAVA_VERSION=26-ea+32
# Wed, 28 Jan 2026 22:11:40 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='99e956807a500a396bc799f5b450e79c295bccece78ae9ca67f3e75646d3a099'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef6d53835db7740daeda9be917698b14f742df288966e4985504f7f2e465ad0b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 28 Jan 2026 22:11:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7277b006798b7010f7a3c16433d0f4ff67bd919446768330eb3bb26f4c1b8392`  
		Last Modified: Wed, 28 Jan 2026 22:12:04 GMT  
		Size: 38.7 MB (38691925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706597df5c79d02c3cc58f5a91f8c62febfc66958b247eb5b033f5dd1d5eaffb`  
		Last Modified: Wed, 28 Jan 2026 22:12:08 GMT  
		Size: 225.8 MB (225785547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-32-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:ddda5519519f15fe942320627c667b35c6c4b35d53cd7c9b5cdba9f877e13e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166a25a7f99e65ee87ec0e4bc331266763a821ea5715d95af1582a2f60748456`

```dockerfile
```

-	Layers:
	-	`sha256:37d0824284b74e213b42ee1ccc20d22522278862428cee7b7a7109c9e6cefdbd`  
		Last Modified: Wed, 28 Jan 2026 22:12:02 GMT  
		Size: 3.7 MB (3653081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7390ec14679b619022c47eb35e5d8b76905c838bba35491336a105cb7a647dd4`  
		Last Modified: Wed, 28 Jan 2026 22:12:01 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-32-jdk` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:b0a862c7030f4c64c53560cc76536ceaf8b1dc180f1c984ba4227d003da51e48
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1720894267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662a4647a293f8ebe9f0a8d12df8470f945e118ddb091f6edeba4f350861b2f3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:06:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:07:29 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:07:30 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 26 Jan 2026 22:07:36 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:07:37 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:07:37 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_windows-x64_bin.zip
# Mon, 26 Jan 2026 22:07:38 GMT
ENV JAVA_SHA256=02a8f8920550b69cdbebb0d7b6eb675d5f597bc5feb7513ae61038c856c19cb8
# Mon, 26 Jan 2026 22:08:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6f0fe5c2ded94d05d8850f2bf11e84d6153343ff1a72da11b95d4b3c0f58dd`  
		Last Modified: Mon, 26 Jan 2026 22:08:30 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430b534904c1592a1870feed501cbaa637066644d88aa3cb2f832f9f03a44dc8`  
		Last Modified: Mon, 26 Jan 2026 22:08:30 GMT  
		Size: 413.3 KB (413332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d1eadc999be4fee3969bbbc6e5dee497f8375711163b205b725063626604f`  
		Last Modified: Mon, 26 Jan 2026 22:08:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c194857e881cea86ab58516eeabed9b9ba428e65fb28777d03debc89f42481`  
		Last Modified: Mon, 26 Jan 2026 22:08:30 GMT  
		Size: 399.0 KB (398953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d562648f8bbd99fa227cee1815c1cf6aa0ab41b2c0b83667d821387bd9223d`  
		Last Modified: Mon, 26 Jan 2026 22:08:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e9512af59058ee7507f7eec02856eed7fb6506bd81b68897169d482bc6aae1`  
		Last Modified: Mon, 26 Jan 2026 22:08:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642a5fe9c3d2c0a7d6bca0129a914333dd883f14be305363b12af6815f48b3e1`  
		Last Modified: Mon, 26 Jan 2026 22:08:28 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788e599a8d87366f32a34a1e6815d12514a6ea23411478529cfd3ac9dc25421`  
		Last Modified: Mon, 26 Jan 2026 22:08:44 GMT  
		Size: 224.3 MB (224313810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fc57a17f0c78c89c6ae4f8098299cbe8028b9aeb2a61958fda26192a2afa76`  
		Last Modified: Mon, 26 Jan 2026 22:08:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-32-jdk` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:58d9bbf5142fd55adb994619c7c1aa1d432ced27da1b80cac88d2d1ee815e696
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2060788968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b397fa34425cd7e164d9992f2cc6cbd9dc32c76a82cf3f92f95ab4e64e8707`
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
ENV JAVA_HOME=C:\openjdk-26
# Mon, 26 Jan 2026 22:08:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:58 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:09:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_windows-x64_bin.zip
# Mon, 26 Jan 2026 22:09:01 GMT
ENV JAVA_SHA256=02a8f8920550b69cdbebb0d7b6eb675d5f597bc5feb7513ae61038c856c19cb8
# Mon, 26 Jan 2026 22:10:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:10:21 GMT
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fa8db78906ea6fbf10041de1ed15ff81c180a21a4f65ae404226dece2460a4`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 503.7 KB (503709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284a6959273d9ba6a25688b512b9013204f189023c9eb7022f9ac08eaf3d26c6`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06de4c3e24ae6000dddba236b23f22ef27aeb99e16ced180f3cda2d49aeb55e8`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 351.8 KB (351761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5206495a19cb6b0ce0a5a53657bf7ae9d3536b05259466c892ca6884b49b93ee`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6ec380a32cfcc46f5ff1f36e377ca8a30b0614e5807d08cca274d6ef6750bf`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc845909244c84e6066c4b57225fc7f4dc3a13926e3980d8eeb906e647e19c66`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f814cb8506ce154ec001ddaf56ceef947e401882612c8e7b2143cbbede126153`  
		Last Modified: Mon, 26 Jan 2026 22:10:43 GMT  
		Size: 224.3 MB (224266490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe6edc21e1d71fac10b10e5aa52ee2b1c4b76aeaf2bb358b9bf9c922992b5f1`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
