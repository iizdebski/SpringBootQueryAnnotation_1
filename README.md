# SpringBootQueryAnnotation_1

@Query SpringBoot JPA JPQL

MySQL - namedquery, table - persons_table;

username = root, password = root

public interface PeopleManangementDao extends CrudRepository<Person, Integer>{

@Query(value = "SELECT p FROM Person p WHERE p.lastName=?1")

List<Person> getPeronInfoByLastName(String lastName);

@Query(value = "SELECT p FROM Person p WHERE p.firstName=?1 AND email=?2")

List<Person> findByFirstNameAndEmail(String firstName,String email);
