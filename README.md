from abc import ABC, abstractmethod

class Figura(ABC):
    @abstractmethod
    def calcular_perimetro(self) -> float:
        pass

    @abstractmethod
    def calcular_area(self) -> float:
        pass

    @abstractmethod
    def obtener_nombre(self) -> str:
        pass

class Cuadrado(Figura):
    def __init__(self, lado: float):
        self.lado = lado

    def calcular_perimetro(self) -> float:
        return 4 * self.lado

    def calcular_area(self) -> float:
        return self.lado ** 2

    def obtener_nombre(self) -> str:
        return "Cuadrado"

if __name__ == "__main__":
    c = Cuadrado(5)
    print(c.obtener_nombre())
    print(f"Perímetro: {c.calcular_perimetro():.2f}")
    print(f"Área: {c.calcular_area():.2f}")
